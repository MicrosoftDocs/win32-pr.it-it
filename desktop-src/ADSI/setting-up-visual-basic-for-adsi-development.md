---
title: Configurazione di Visual Basic 6,0 per lo sviluppo ADSI
description: In questo argomento viene illustrato come configurare Visual Basic in Visual Studio per sviluppare un'applicazione ADSI.
ms.assetid: 167e89d7-80a3-4cc2-b79c-3744c1b184d6
ms.tgt_platform: multiple
keywords:
- Configurazione di Visual Basic per lo sviluppo ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e6b1f39ec06d3716beab750dbf2a522d4c18cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855246"
---
# <a name="setting-up-visual-basic-60-for-adsi-development"></a><span data-ttu-id="6c15e-104">Configurazione di Visual Basic 6,0 per lo sviluppo ADSI</span><span class="sxs-lookup"><span data-stu-id="6c15e-104">Setting Up Visual Basic 6.0 for ADSI Development</span></span>

<span data-ttu-id="6c15e-105">**Configurazione dell'ambiente di sviluppo Microsoft Visual Studio 2010 per Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="6c15e-105">**Setting Up the Microsoft Visual Studio 2010 Development Environment For Visual Basic**</span></span>

1.  <span data-ttu-id="6c15e-106">Avviare Visual Studio 2010.</span><span class="sxs-lookup"><span data-stu-id="6c15e-106">Start Visual Studio 2010.</span></span>
2.  <span data-ttu-id="6c15e-107">Creare un nuovo progetto Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6c15e-107">Create a new Visual Basic project.</span></span>
3.  <span data-ttu-id="6c15e-108">Aggiungere un riferimento alla libreria dei tipi di servizi di **dominio Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="6c15e-108">Add a reference to the **Active DS Type Library**.</span></span>
    > [!Note]  
    > <span data-ttu-id="6c15e-109">Se non è necessaria l'associazione iniziale di oggetti COM, ignorare questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="6c15e-109">If you do not require early COM object binding, ignore this step.</span></span>

     

    1.  <span data-ttu-id="6c15e-110">Selezionare **progetto \| Aggiungi riferimento**.</span><span class="sxs-lookup"><span data-stu-id="6c15e-110">Select **Project \| Add Reference**.</span></span>
    2.  <span data-ttu-id="6c15e-111">Selezionare la scheda **com** .</span><span class="sxs-lookup"><span data-stu-id="6c15e-111">Select the **COM** tab.</span></span>
    3.  <span data-ttu-id="6c15e-112">Selezionare **Active DS Type Library**.</span><span class="sxs-lookup"><span data-stu-id="6c15e-112">Select **Active DS Type Library**.</span></span>

4.  <span data-ttu-id="6c15e-113">Iniziare la programmazione con ADSI.</span><span class="sxs-lookup"><span data-stu-id="6c15e-113">Begin programming with ADSI.</span></span>

<span data-ttu-id="6c15e-114">Prima di iniziare, accedere a un dominio Windows.</span><span class="sxs-lookup"><span data-stu-id="6c15e-114">Before you begin, log on to a Windows domain.</span></span> <span data-ttu-id="6c15e-115">È necessario disporre dell'autorizzazione per modificare il database di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6c15e-115">You must have permission to modify the Active Directory database.</span></span> <span data-ttu-id="6c15e-116">Per impostazione predefinita, l'amministratore dispone di questo privilegio.</span><span class="sxs-lookup"><span data-stu-id="6c15e-116">By default, the Administrator has this privilege.</span></span>

<span data-ttu-id="6c15e-117">**Applicazione Visual Basic 6,0 di esempio: modifica di FullName e Description per un utente**</span><span class="sxs-lookup"><span data-stu-id="6c15e-117">**A Sample Visual Basic 6.0 Application: Modifying FullName and Description for a User**</span></span>

1.  <span data-ttu-id="6c15e-118">Seguire i passaggi precedenti per creare un progetto di Visual Basic eseguibile standard.</span><span class="sxs-lookup"><span data-stu-id="6c15e-118">Follow the previous steps to create a standard executable Visual Basic project.</span></span>
2.  <span data-ttu-id="6c15e-119">Fare doppio clic sul form.</span><span class="sxs-lookup"><span data-stu-id="6c15e-119">Double-click the Form.</span></span> <span data-ttu-id="6c15e-120">In \_ caricamento del modulo digitare quanto segue.</span><span class="sxs-lookup"><span data-stu-id="6c15e-120">In Form\_Load, type the following.</span></span> <span data-ttu-id="6c15e-121">È necessario sostituire la stringa "LDAP://CN = SergioMelchiori, CN = Users, DC = Fabrikam, DC = com" con ADsPath di un utente esistente in un contenitore del dominio.</span><span class="sxs-lookup"><span data-stu-id="6c15e-121">You must replace the "LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com" string with the ADsPath of an existing user in a container in your domain.</span></span> <span data-ttu-id="6c15e-122">Creare un account utente di test che può essere modificato a questo scopo.</span><span class="sxs-lookup"><span data-stu-id="6c15e-122">Create a test user account that can be modified for this purpose.</span></span>
    ```VB
    '------------------------------------------------------------
    ' This code example is used to set the FullName and Description
    '------------------------------------------------------------
    Dim usr As IADsUser

    ' Bind to a user object.
    Set usr = GetObject("LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com")

    usr.FullName = "Jeff Smith"
    usr.Description = "A user for fabrikam.com" 
    usr.SetInfo ' Commit the changes to the directory
    ```

    

3.  <span data-ttu-id="6c15e-123">Premere **<F5>** per eseguire il programma.</span><span class="sxs-lookup"><span data-stu-id="6c15e-123">Press **<F5>** to run the program.</span></span>
4.  <span data-ttu-id="6c15e-124">Per verificare le modifiche, usare lo strumento di gestione Active Directory utenti e computer.</span><span class="sxs-lookup"><span data-stu-id="6c15e-124">To verify changes, use the Active Directory Users and Computers management tool.</span></span> <span data-ttu-id="6c15e-125">Per ulteriori informazioni sull'utilizzo di ADSI e Visual Basic, vedere [accesso Active Directory utilizzando Visual Basic](accessing-active-directory-using-visual-basic.md).</span><span class="sxs-lookup"><span data-stu-id="6c15e-125">For more information about using ADSI and Visual Basic, see [Accessing Active Directory Using Visual Basic](accessing-active-directory-using-visual-basic.md).</span></span>

 

 




