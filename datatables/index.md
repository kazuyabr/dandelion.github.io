---
layout: datatables
menu: home
---

<img src="/assets/images/logo_DataTables.jpg" style="float: right;" />

**Dandelion-DataTables** is a component of the free and Open Source web framework [Dandelion](http://dandelion.github.com/).
<br />
It allows you to quickly create full-featured HTML table based on the amazing [DataTables](http://datatables.net "DataTables") jQuery plugin.

Writing table in your Java/JEE based web application has never been so easy thanks to all the features (compression, aggregation, export), themes, plugins and template engines integration : JSP and [Thymeleaf](http://www.thymeleaf.org)! 

<br />
#### How to use it?
<h5>With JSP taglib</h5>
Quiet simply. Once the taglib definition included in your JSP, write the following lines :

    <datatables:table id="myTableId" data="${persons}">
        <datatables:column title="Id" property="id" />
        <datatables:column title="FirstName" property="firstName" />
        <datatables:column title="LastName" property="lastName" />
        <datatables:column title="Street" property="address.street1" />
        <datatables:column title="Mail" property="mail" />
    </datatables:table>

<h5>With Thymeleaf</h5>
Quiet simply too! Once the **Dandelion-DataTables** dialect and the namespace declaration added, write the following lines :

    <table id="myTableId" dt:table="true">
        <thead>
            <tr>
                <th>Id</th>
                <th>Firstname</th>
                <th>Lastname</th>
                <th>Street</th>
                <th>Mail</th>
            </tr>
        </thead>
        <tbody>
            <tr th:each="person : ${persons}">
                <td th:text="${person.id}">1</td>
                <td th:text="${person.firstName}">John</td>
                <td th:text="${person.lastName}">Doe</td>
                <td th:text="${person.address.street1}">Nobody knows !</td>
                <td th:text="${person.mail}">john@doe.com</td>
            </tr>
        </tbody>
    </table>

<h5>Result</h5>
 
As a result, you\'ll have the following full-featured HTML table!

<table id="exampleTable"><thead><tr><th>Id</th><th>FirstName</th><th>LastName</th><th>Street</th><th>Mail</th></tr></thead><tfoot><tr><th></th><th></th><th></th><th></th><th></th></tr></tfoot><tbody><tr><td>1</td><td>Selma</td><td>Maldonado</td><td>Ap #351-1812 Eu, Ave</td><td>venenatis@Duisvolutpat.com</td></tr><tr><td>2</td><td>Vanna</td><td>Salas</td><td>947-3605 Feugiat. St.</td><td>bibendum.fermentum.metus@ante.ca</td></tr><tr><td>3</td><td>Noble</td><td>Rosales</td><td>1389 Aliquam, St.</td><td>Duis.cursus.diam@dolorelitpellentesque.ca</td></tr><tr><td>4</td><td>Nehru</td><td>Gonzalez</td><td>P.O. Box 374, 9474 Lacinia Street</td><td>tellus.non.magna@pede.edu</td></tr><tr><td>5</td><td>Calista</td><td>Hill</td><td>8966 Eu Road</td><td>enim.Etiam.imperdiet@sitametrisus.co.uk</td></tr><tr><td>6</td><td>Chava</td><td>Wilder</td><td>317-8683 Ligula. St.</td><td>lacus.vestibulum@incursus.edu</td></tr><tr><td>7</td><td>Oliver</td><td>Rivas</td><td>6489 Sed Ave</td><td>velit@pedemalesuada.co.uk</td></tr><tr><td>8</td><td>Lila</td><td>Morrow</td><td>8438 Viverra. Ave</td><td>Mauris.eu.turpis@In.ca</td></tr><tr><td>9</td><td>Yen</td><td>Vargas</td><td>P.O. Box 722, 6079 Eu St.</td><td>odio@Donec.net</td></tr><tr><td>10</td><td>Lee</td><td>Graves</td><td>211-4991 Dictum Road</td><td>velit@vitae.co.uk</td></tr><tr><td>11</td><td>Shelby</td><td>Cabrera</td><td>8307 Vehicula. St.</td><td>magna.a.tortor@lobortisrisusIn.ca</td></tr><tr><td>12</td><td>Demetrius</td><td>Barber</td><td>5637 Vitae Street</td><td>lectus.Cum.sociis@egestasligula.org</td></tr><tr><td>13</td><td>Joelle</td><td>Peck</td><td>8552 Placerat, St.</td><td>urna.suscipit.nonummy@diam.com</td></tr><tr><td>14</td><td>Fredericka</td><td>Pena</td><td>5132 Venenatis Road</td><td>Sed.pharetra.felis@litoratorquentper.edu</td></tr><tr><td>15</td><td>Susan</td><td>Hensley</td><td>8331 Est, Street</td><td>mus.Aenean@inaliquetlobortis.org</td></tr><tr><td>16</td><td>Ivana</td><td>Day</td><td>P.O. Box 629, 6589 Ultrices Avenue</td><td>urna.Vivamus@natoquepenatibus.net</td></tr><tr><td>17</td><td>Lilah</td><td>Pena</td><td>P.O. Box 782, 3437 Cursus. Ave</td><td>nec@Sed.com</td></tr><tr><td>18</td><td>Gabriel</td><td>Morse</td><td>542-8737 Convallis Street</td><td>pellentesque.tellus@Seddictum.com</td></tr><tr><td>19</td><td>McKenzie</td><td>Mejia</td><td>435-3099 Porta Av.</td><td>velit@arcu.co.uk</td></tr><tr><td>20</td><td>Joy</td><td>Hernandez</td><td>967-1885 Tempor Av.</td><td>est@necmollisvitae.com</td></tr><tr><td>21</td><td>Logan</td><td>Velazquez</td><td>P.O. Box 283, 1560 Aenean Avenue</td><td>Mauris@urnajusto.org</td></tr><tr><td>22</td><td>Paki</td><td>Carpenter</td><td>P.O. Box 562, 9899 Adipiscing Road</td><td>nibh.lacinia.orci@odiovel.org</td></tr><tr><td>23</td><td>Boris</td><td>Mclaughlin</td><td>P.O. Box 403, 525 Sem Street</td><td>eros@purusNullamscelerisque.co.uk</td></tr><tr><td>24</td><td>Ainsley</td><td>Henry</td><td>P.O. Box 322, 1581 Etiam Rd.</td><td>mauris.sagittis.placerat@sitametluctus.co.uk</td></tr><tr><td>25</td><td>Lars</td><td>Weiss</td><td>213-957 Ornare Street</td><td>lacus@nisi.edu</td></tr><tr><td>26</td><td>Amery</td><td>Richardson</td><td>Ap #917-7801 Metus. Road</td><td>eget.laoreet@morbitristiquesenectus.org</td></tr><tr><td>27</td><td>Ivy</td><td>Wagner</td><td>699-6077 Egestas. Road</td><td>magna@massa.ca</td></tr><tr><td>28</td><td>Kaitlin</td><td>Hooper</td><td>P.O. Box 577, 1556 Pede, Avenue</td><td>volutpat.Nulla@risusQuisquelibero.org</td></tr><tr><td>29</td><td>Grady</td><td>Fox</td><td>323-922 Lorem Street</td><td>Nulla@lectusconvallisest.net</td></tr><tr><td>30</td><td>Jesse</td><td>Trujillo</td><td>P.O. Box 977, 8437 Non Street</td><td>nec.cursus@mollisnec.org</td></tr><tr><td>31</td><td>Anika</td><td>Franco</td><td>Ap #150-496 Tellus Rd.</td><td>vel@sed.com</td></tr><tr><td>32</td><td>Haviva</td><td>Lewis</td><td>872-4546 Egestas. St.</td><td>dignissim.magna.a@faucibusMorbi.ca</td></tr><tr><td>33</td><td>Gisela</td><td>Clayton</td><td>659-3340 Litora Road</td><td>volutpat.nunc@ipsumSuspendissenon.co.uk</td></tr><tr><td>34</td><td>Quinn</td><td>Nielsen</td><td>P.O. Box 249, 7823 Elementum, Rd.</td><td>Cras.vulputate@magna.ca</td></tr><tr><td>35</td><td>Samantha</td><td>Alexander</td><td>P.O. Box 915, 3911 Cursus Avenue</td><td>Curae;.Phasellus.ornare@loremDonec.ca</td></tr><tr><td>36</td><td>Sage</td><td>Hurley</td><td>3580 Metus St.</td><td>non@lectusNullamsuscipit.co.uk</td></tr><tr><td>37</td><td>Leslie</td><td>Coleman</td><td>Ap #465-5758 Sed Avenue</td><td>convallis.convallis@dapibus.edu</td></tr><tr><td>38</td><td>Gil</td><td>Garza</td><td>548-8537 Imperdiet Ave</td><td>nunc.nulla.vulputate@vulputatenisi.com</td></tr><tr><td>39</td><td>Richard</td><td>Grimes</td><td>571 Tempus St.</td><td>mi.Aliquam.gravida@dictum.org</td></tr><tr><td>40</td><td>Xavier</td><td>Hebert</td><td>959-1515 Quis Av.</td><td>dictum.eu.placerat@Aliquamfringilla.net</td></tr><tr><td>41</td><td>Laurel</td><td>Newman</td><td>Ap #311-3077 Lacus Rd.</td><td>et@aliquetlibero.ca</td></tr><tr><td>42</td><td>Grace</td><td>Robinson</td><td>Ap #347-1394 Eget Rd.</td><td>lobortis.augue.scelerisque@Etiamvestibulum.com</td></tr><tr><td>43</td><td>Holly</td><td>Terry</td><td>Ap #437-6599 Tempor Ave</td><td>In@sollicitudina.edu</td></tr><tr><td>44</td><td>Lael</td><td>Simmons</td><td>5541 Dis St.</td><td>eu@pellentesquemassa.net</td></tr><tr><td>45</td><td>Chelsea</td><td>Schroeder</td><td>943-9091 Urna. Av.</td><td>ligula@rutrumurnanec.com</td></tr><tr><td>46</td><td>Isabella</td><td>Poole</td><td>P.O. Box 853, 7299 Ornare, Road</td><td>mattis.semper@iaculisaliquet.net</td></tr><tr><td>47</td><td>Marvin</td><td>Carpenter</td><td>8116 Metus. Rd.</td><td>nulla.Integer@inaliquet.org</td></tr><tr><td>48</td><td>Steel</td><td>Ruiz</td><td>P.O. Box 447, 5754 Montes, Ave</td><td>odio.Phasellus.at@Nullamsuscipit.org</td></tr><tr><td>49</td><td>Dennis</td><td>Black</td><td>P.O. Box 487, 4030 Massa Avenue</td><td>quam@bibendum.org</td></tr><tr><td>50</td><td>Mari</td><td>Gill</td><td>2170 Pellentesque Avenue</td><td>facilisis.non.bibendum@insodales.ca</td></tr><tr><td>51</td><td>Jared</td><td>Wolfe</td><td>375 Amet, Road</td><td>Sed.auctor.odio@euturpis.ca</td></tr><tr><td>52</td><td>Uriel</td><td>Walter</td><td>P.O. Box 143, 9222 Fermentum Ave</td><td>Cras.interdum@Crasdictum.edu</td></tr><tr><td>53</td><td>Ahmed</td><td>Heath</td><td>5457 Vivamus Rd.</td><td>mi.pede.nonummy@erosturpis.com</td></tr><tr><td>54</td><td>Wilma</td><td>James</td><td>Ap #420-8962 Ut Avenue</td><td>Vestibulum.ut.eros@rhoncusNullamvelit.net</td></tr><tr><td>55</td><td>Sybill</td><td>Conley</td><td>Ap #327-962 Lacinia. Av.</td><td>id@estvitaesodales.net</td></tr><tr><td>56</td><td>Kristen</td><td>Sampson</td><td>3345 Facilisis St.</td><td>parturient.montes.nascetur@infelisNulla.net</td></tr><tr><td>57</td><td>Chester</td><td>Peck</td><td>379-696 Interdum. Road</td><td>ultrices@sapienCras.ca</td></tr><tr><td>58</td><td>Samson</td><td>Moran</td><td>P.O. Box 668, 6707 Et Av.</td><td>Proin.sed.turpis@leoelementumsem.co.uk</td></tr><tr><td>59</td><td>Indigo</td><td>Parker</td><td>7470 Id, Rd.</td><td>ante@tacitisociosqu.org</td></tr><tr><td>60</td><td>Dai</td><td>George</td><td>7623 Faucibus Av.</td><td>pede.Cum.sociis@temporbibendum.org</td></tr><tr><td>61</td><td>Shelley</td><td>Hickman</td><td>311-2493 Dictum St.</td><td>dis.parturient@Maurisblandit.org</td></tr><tr><td>62</td><td>Jennifer</td><td>Ramirez</td><td>489 Luctus Ave</td><td>convallis.convallis@pedeultricesa.edu</td></tr><tr><td>63</td><td>Claire</td><td>Pruitt</td><td>570-6292 Cras St.</td><td>velit@augueeu.ca</td></tr><tr><td>64</td><td>Raja</td><td>Stuart</td><td>9253 Sit Av.</td><td>dapibus@Sed.com</td></tr><tr><td>65</td><td>Alika</td><td>Wells</td><td>449-1169 Eu Street</td><td>sit.amet.diam@aliquetdiamSed.com</td></tr><tr><td>66</td><td>Lynn</td><td>Holloway</td><td>P.O. Box 609, 8735 Luctus Av.</td><td>purus@enimconsequatpurus.com</td></tr><tr><td>67</td><td>Meredith</td><td>Shaw</td><td>P.O. Box 441, 5797 Sem Rd.</td><td>mauris.sagittis.placerat@idnuncinterdum.ca</td></tr><tr><td>68</td><td>Brennan</td><td>Paul</td><td>P.O. Box 160, 8976 Sagittis Ave</td><td>facilisis.lorem.tristique@vulputateposuerevulputate.co.uk</td></tr><tr><td>69</td><td>Berk</td><td>Reynolds</td><td>P.O. Box 462, 8364 Interdum. Ave</td><td>consequat.nec.mollis@nequetellusimperdiet.ca</td></tr><tr><td>70</td><td>Hedy</td><td>Atkins</td><td>P.O. Box 826, 8259 Dolor St.</td><td>risus.Duis.a@vitaediam.com</td></tr><tr><td>71</td><td>Raya</td><td>Hunt</td><td>Ap #877-9986 Velit Street</td><td>in@velquam.ca</td></tr><tr><td>72</td><td>Darrel</td><td>Potter</td><td>Ap #863-9991 Mauris. Ave</td><td>venenatis.a.magna@felisDonectempor.org</td></tr><tr><td>73</td><td>Robert</td><td>Cortez</td><td>9832 Quisque Road</td><td>eget@Ut.edu</td></tr><tr><td>74</td><td>Reese</td><td>Joyner</td><td>7272 Ac Av.</td><td>Morbi.accumsan@parturientmontes.ca</td></tr><tr><td>75</td><td>Jeanette</td><td>Park</td><td>P.O. Box 386, 6684 Donec Ave</td><td>pede.ac.urna@ipsumdolorsit.edu</td></tr><tr><td>76</td><td>Alice</td><td>Foreman</td><td>Ap #456-5148 At Street</td><td>lorem.eu@feugiat.edu</td></tr><tr><td>77</td><td>Lana</td><td>Pacheco</td><td>Ap #764-4979 Sem Street</td><td>elit.pellentesque@urnaconvalliserat.org</td></tr><tr><td>78</td><td>Fitzgerald</td><td>Dorsey</td><td>P.O. Box 697, 8717 Pede. St.</td><td>nulla.Donec@idnuncinterdum.org</td></tr><tr><td>79</td><td>Amy</td><td>Marshall</td><td>Ap #481-1909 A Av.</td><td>ad.litora@egestasAliquam.net</td></tr><tr><td>80</td><td>Dean</td><td>Boyer</td><td>723-8147 Nullam Rd.</td><td>Nunc@uterosnon.com</td></tr><tr><td>81</td><td>Madeline</td><td>Fernandez</td><td>541-6418 Tincidunt Ave</td><td>Proin.sed.turpis@Nulladignissim.com</td></tr><tr><td>82</td><td>Tashya</td><td>Horton</td><td>Ap #825-7771 Cum Av.</td><td>Maecenas.malesuada@Aliquamtinciduntnunc.com</td></tr><tr><td>83</td><td>Genevieve</td><td>Yang</td><td>962-5661 Libero. St.</td><td>molestie@primis.co.uk</td></tr><tr><td>84</td><td>Kiona</td><td>Gates</td><td>Ap #438-8624 Urna Av.</td><td>velit.Cras@lobortis.edu</td></tr><tr><td>85</td><td>Xaviera</td><td>Guerrero</td><td>386-2394 Sem Rd.</td><td>ac.turpis@ipsumac.co.uk</td></tr><tr><td>86</td><td>Raja</td><td>Frederick</td><td>506-4514 Urna Road</td><td>id@incursuset.ca</td></tr><tr><td>87</td><td>Andrew</td><td>Langley</td><td>222-4261 A Ave</td><td>lorem.ipsum.sodales@vulputateullamcorper.org</td></tr><tr><td>88</td><td>Phelan</td><td>Hicks</td><td>209-4174 Vehicula Rd.</td><td>volutpat.Nulla.dignissim@Phasellus.com</td></tr><tr><td>89</td><td>Glenna</td><td>Bright</td><td>P.O. Box 570, 2040 Dictum Street</td><td>sagittis.felis@orci.net</td></tr><tr><td>90</td><td>Ignatius</td><td>Daniels</td><td>724-5977 Arcu Rd.</td><td>fames.ac@pede.com</td></tr><tr><td>91</td><td>Cadman</td><td>Peck</td><td>550-1348 Arcu. St.</td><td>Aliquam@nuncsed.ca</td></tr><tr><td>92</td><td>Ivan</td><td>Wilder</td><td>P.O. Box 145, 111 Accumsan Rd.</td><td>magna@massarutrum.co.uk</td></tr><tr><td>93</td><td>Jolie</td><td>Jacobson</td><td>9487 A, Road</td><td>non.sollicitudin@Pellentesqueut.edu</td></tr><tr><td>94</td><td>Michael</td><td>Forbes</td><td>8488 Neque St.</td><td>odio.Aliquam@rutrumloremac.net</td></tr><tr><td>95</td><td>Erin</td><td>Bullock</td><td>Ap #345-6440 Tristique Street</td><td>Nunc.sollicitudin@tempusscelerisquelorem.edu</td></tr><tr><td>96</td><td>Vladimir</td><td>Morton</td><td>2665 Orci Rd.</td><td>consequat.enim.diam@consequatnecmollis.co.uk</td></tr><tr><td>97</td><td>Iola</td><td>Holloway</td><td>607-3536 Laoreet Rd.</td><td>mattis.Cras.eget@enim.co.uk</td></tr><tr><td>98</td><td>Amelia</td><td>Savage</td><td>Ap #309-2802 Integer Av.</td><td>ultrices@dictum.org</td></tr><tr><td>99</td><td>Brendan</td><td>Romero</td><td>7489 Sapien. Avenue</td><td>morbi@Aeneansed.co.uk</td></tr><tr><td>100</td><td>Ralph</td><td>Charles</td><td>Ap #745-9871 Elit. St.</td><td>tincidunt.vehicula.risus@eratnequenon.edu</td></tr></tbody></table>

<br />
#### Getting started
Feel free to browse/clone/fork the demo apps!

 * [JSP demo](https://github.com/Dandelion/dandelion-samples/tree/master/datatables-jsp)
 * [Thymeleaf demo](https://github.com/Dandelion/dandelion-samples/tree/master/datatables-thymeleaf)

<br />
#### Bug / Enhancement
For any issues or enhancements, please use the dedicated [Github issues repo](https://github.com/dandelion/issues/issues). 

<br />
####Forum
If you need support or want to discuss any issues you might be having with <strong>Dandelion</strong> or <strong>Dandelion-DataTables</strong>, the doors of the [forum](./forum.html) are wide open!  

<br />
#### License
**Dandelion-DataTables** is released under the [BSD 3-Clause](http://opensource.org/licenses/BSD-3-Clause) licence, i.e. you can do almost everything you want with it.

<link rel="stylesheet" href="http://ajax.aspnetcdn.com/ajax/jquery.dataTables/1.9.4/css/jquery.dataTables.css" />
<script src="http://ajax.aspnetcdn.com/ajax/jquery.dataTables/1.9.4/jquery.dataTables.min.js">
</script>
<script type="text/javascript" src="/assets/js/example.js">
</script>