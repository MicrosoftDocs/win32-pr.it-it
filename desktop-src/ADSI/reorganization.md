---
title: Riorganizzazione
description: L'organizzazione vendite è stata spostata in una nuova organizzazione \ 8212; \ 0034; Vendite e supporto. \ 0034; Julie Bankert è stato promosso a vicepresidente e avrà la nuova organizzazione.
ms.assetid: 38b05d0b-2739-43c2-aac7-7555a5bfbc91
ms.tgt_platform: multiple
keywords:
- Riorganizzazione di ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587f3de34738814b34ad250bb00bb7b71121d65c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044059"
---
# <a name="reorganization"></a><span data-ttu-id="e7cd3-105">Riorganizzazione</span><span class="sxs-lookup"><span data-stu-id="e7cd3-105">Reorganization</span></span>

<span data-ttu-id="e7cd3-106">L'organizzazione vendite è stata spostata in una nuova organizzazione, ovvero "vendite e supporto".</span><span class="sxs-lookup"><span data-stu-id="e7cd3-106">The sales organization has moved to a new organization — "Sales and Support."</span></span> <span data-ttu-id="e7cd3-107">Julie Bankert è stato promosso a vicepresidente e avrà la nuova organizzazione.</span><span class="sxs-lookup"><span data-stu-id="e7cd3-107">Julie Bankert has been promoted to vice president and will lead the new organization.</span></span> <span data-ttu-id="e7cd3-108">Joe worden, l'amministratore dell'organizzazione, deve spostare l'unità organizzativa vendite in una nuova unità organizzativa, vendite e supporto.</span><span class="sxs-lookup"><span data-stu-id="e7cd3-108">Joe Worden, the enterprise administrator, must move Sales OU to a new OU, Sales and Support.</span></span>


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=COM")
Set salesSupport = dom.Create("organizationalUnit", "CN=Sales and Support")
Set sales = salesSupport.MoveHere("LDAP://OU=Sales,DC=Fabrikam,DC=COM", vbNullString)
```



<span data-ttu-id="e7cd3-109">Con questo esempio di codice, tutti gli oggetti nell'unità organizzativa Sales, incluse le unità organizzative secondarie, vengono spostati nella nuova unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="e7cd3-109">With this code example, all objects in the sales organizational unit, including the sub-organizational units, are moved to the new organizational unit.</span></span>

<span data-ttu-id="e7cd3-110">Ora Joe può spostare Julie nell'unità organizzativa Sales and support.</span><span class="sxs-lookup"><span data-stu-id="e7cd3-110">Now, Joe can move Julie into the Sales and Support organizational unit.</span></span>


```VB
Set usr = salesSupport.MoveHere("LDAP://CN=Julie Bankert,OU=Sales,OU=Sales and Support,DC=Fabrikam,DC=COM")
usr.Put "title", "Vice President"
usr.SetInfo
```



<span data-ttu-id="e7cd3-111">Tenere presente che il collegamento Manager-Direct report tra Julie Bankert e Chris Gray viene aggiornato automaticamente da Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e7cd3-111">Be aware that the manager-direct report link between Julie Bankert and Chris Gray is automatically updated by Active Directory.</span></span>

<span data-ttu-id="e7cd3-112">**Per creare un report Active Directory**</span><span class="sxs-lookup"><span data-stu-id="e7cd3-112">**To create an Active Directory report**</span></span>

1.  <span data-ttu-id="e7cd3-113">Aprire Visual Basic versione 6,0 e, quando viene richiesto il tipo di progetto, selezionare **progetto dati**.</span><span class="sxs-lookup"><span data-stu-id="e7cd3-113">Open Visual Basic version 6.0, and when prompted for the project type, select **Data Project**.</span></span>
2.  <span data-ttu-id="e7cd3-114">In **progetto dati** fare doppio clic su **dati Environment1**.</span><span class="sxs-lookup"><span data-stu-id="e7cd3-114">On **Data Project**, double-click **Data Environment1**.</span></span>
3.  <span data-ttu-id="e7cd3-115">Nella finestra **ambiente dati** fare clic con il pulsante destro del mouse sull'oggetto connessione **(Connection1)** e scegliere **proprietà**.</span><span class="sxs-lookup"><span data-stu-id="e7cd3-115">On the **Data Environment** window, right-click the connection object **(Connection1)** and select **Properties**.</span></span>
4.  <span data-ttu-id="e7cd3-116">Selezionare **OLE DB provider per servizi directory Microsoft**, quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="e7cd3-116">Select **OLE DB Provider for Microsoft Directory Services**, and click **Next**.</span></span>
5.  <span data-ttu-id="e7cd3-117">Selezionare **Usa sicurezza integrata di Windows NT**, quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7cd3-117">Select **Use Windows NT Integrated security**, and click **OK**.</span></span> <span data-ttu-id="e7cd3-118">Viene creato un oggetto Connection.</span><span class="sxs-lookup"><span data-stu-id="e7cd3-118">This creates a connection object.</span></span>
6.  <span data-ttu-id="e7cd3-119">Fare di nuovo clic con il pulsante destro del mouse sulla finestra **ambiente dati** per selezionare **Aggiungi comando**.</span><span class="sxs-lookup"><span data-stu-id="e7cd3-119">Right-click the **Data Environment** window again to select **Add Command**.</span></span> <span data-ttu-id="e7cd3-120">Fare clic con il pulsante destro del mouse sull'oggetto **Command1** e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="e7cd3-120">Right-click the **Command1** object and select **Properties**.</span></span> <span data-ttu-id="e7cd3-121">Verrà visualizzata la finestra di dialogo **Proprietà Command1** seguente.</span><span class="sxs-lookup"><span data-stu-id="e7cd3-121">The following **Command1 Properties** dialog box will appear.</span></span>

    ![finestra di dialogo Proprietà Command1](images/adadsi3.png)

7.  <span data-ttu-id="e7cd3-123">Fare clic sul pulsante di opzione **istruzione SQL** e digitare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="e7cd3-123">Click the **SQL Statement** option button and type the following:</span></span>

    <span data-ttu-id="e7cd3-124">SELECT Name, telephoneNumber FROM "LDAP://DC = Fabrikam, DC = com" WHERE objectCategory = "person" e objectClass = "User"</span><span class="sxs-lookup"><span data-stu-id="e7cd3-124">SELECT Name,telephoneNumber FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectCategory='Person' AND objectClass='user'</span></span>

    <span data-ttu-id="e7cd3-125">Viene creato l'oggetto **Command** .</span><span class="sxs-lookup"><span data-stu-id="e7cd3-125">The **Command** object is created.</span></span> <span data-ttu-id="e7cd3-126">Aggiungere l'oggetto **Command** al report.</span><span class="sxs-lookup"><span data-stu-id="e7cd3-126">Add the **Command** object to the report.</span></span>

8.  <span data-ttu-id="e7cd3-127">Fare doppio clic su **Data Report1** dalla finestra del **progetto** .</span><span class="sxs-lookup"><span data-stu-id="e7cd3-127">Double-click **Data Report1** from the **Project** window.</span></span>
9.  <span data-ttu-id="e7cd3-128">Trascinare l'oggetto **Command1** dalla finestra **DataEnvironment1** nella sezione **Dettagli** della finestra **report dati** .</span><span class="sxs-lookup"><span data-stu-id="e7cd3-128">Drag the **Command1** object from the **DataEnvironment1** window to the **Detail** section in the **Data Report** window.</span></span>
10. <span data-ttu-id="e7cd3-129">In **Proprietà DataReport1** selezionare **DataEnvironment1** dal menu a discesa per **origine dati** e selezionare **Command1** nel campo **DataMember** .</span><span class="sxs-lookup"><span data-stu-id="e7cd3-129">On **DataReport1 Properties**, for **DataSource**, select **DataEnvironment1** from the pull-down menu, and select **Command1** in the **DataMember** field.</span></span>
11. <span data-ttu-id="e7cd3-130">Nella finestra del progetto fare clic con il pulsante destro del mouse su **progetto dati**, quindi scegliere **Proprietà Dataproject**.</span><span class="sxs-lookup"><span data-stu-id="e7cd3-130">On the project window, right-click **Data Project**, and select **DataProject Properties**.</span></span>
12. <span data-ttu-id="e7cd3-131">Nella finestra di dialogo **Proprietà progetto-** progetto, in **oggetto di avvio**, selezionare **DataReport1** dal menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="e7cd3-131">On the **DataProject - Project Properties** dialog window, under **Startup Object**, select **DataReport1** from the pull-down menu.</span></span> <span data-ttu-id="e7cd3-132">Fare clic su **OK** per salvare.</span><span class="sxs-lookup"><span data-stu-id="e7cd3-132">Click **OK** to save.</span></span>
13. <span data-ttu-id="e7cd3-133">Compilazione.</span><span class="sxs-lookup"><span data-stu-id="e7cd3-133">Compile.</span></span> <span data-ttu-id="e7cd3-134">Verrà visualizzata la finestra di dialogo **DataReport1** seguente.</span><span class="sxs-lookup"><span data-stu-id="e7cd3-134">The following **DataReport1** dialog box will appear.</span></span>

    ![finestra di dialogo DataReport1](images/adadsi4.png)

## <a name="related-topics"></a><span data-ttu-id="e7cd3-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e7cd3-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7cd3-137">Unione di dati eterogenei</span><span class="sxs-lookup"><span data-stu-id="e7cd3-137">Joining Heterogeneous Data</span></span>](joining-heterogeneous-data.md)
</dt> </dl>

 

 




