---
title: Configurazione di Visual C++ 6,0 per lo sviluppo ADSI
description: In questo argomento viene illustrato come configurare C++ in Visual Studio in modo da poter sviluppare un'applicazione ADSI.
ms.assetid: 6f1ab3eb-2e0b-4f3e-b93c-e24c8b3b1a27
ms.tgt_platform: multiple
keywords:
- Configurazione di C++ per lo sviluppo ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f2350b88402c921d014b0c93756759a1d0f744
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044054"
---
# <a name="setting-up-visual-c-60-for-adsi-development"></a><span data-ttu-id="bd0b6-104">Configurazione di Visual C++ 6,0 per lo sviluppo ADSI</span><span class="sxs-lookup"><span data-stu-id="bd0b6-104">Setting Up Visual C++ 6.0 for ADSI Development</span></span>

<span data-ttu-id="bd0b6-105">Il sistema di sviluppo Microsoft Visual C++ 6,0 può essere utilizzato per sviluppare applicazioni aziendali.</span><span class="sxs-lookup"><span data-stu-id="bd0b6-105">The Microsoft Visual C++ 6.0 development system can be used to develop enterprise applications.</span></span> <span data-ttu-id="bd0b6-106">Per configurare l'ambiente di Visual C++ 6,0 per lo sviluppo di un'applicazione ADSI, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="bd0b6-106">To set up your Visual C++ 6.0 environment to develop an ADSI application, perform the following steps:</span></span>

<span data-ttu-id="bd0b6-107">**Configurazione dell'ambiente di sviluppo Microsoft Visual C++ 6,0**</span><span class="sxs-lookup"><span data-stu-id="bd0b6-107">**Setting Up the Microsoft Visual C++ 6.0 Development Environment**</span></span>

1.  <span data-ttu-id="bd0b6-108">Puntare al Includi e alla directory della libreria.</span><span class="sxs-lookup"><span data-stu-id="bd0b6-108">Point to the include and library directory.</span></span> <span data-ttu-id="bd0b6-109">Selezionare **strumenti \| Opzioni**.</span><span class="sxs-lookup"><span data-stu-id="bd0b6-109">Select **Tools \| Options**.</span></span> <span data-ttu-id="bd0b6-110">Fare clic sulla scheda **directory** e specificare il percorso dei file di intestazione ADSI.</span><span class="sxs-lookup"><span data-stu-id="bd0b6-110">Click the **Directory** tab, and specify the path to the ADSI header files.</span></span>
2.  <span data-ttu-id="bd0b6-111">Includere il file Activeds. h nel progetto.</span><span class="sxs-lookup"><span data-stu-id="bd0b6-111">Include the Activeds.h file in your project.</span></span>
3.  <span data-ttu-id="bd0b6-112">Aggiungere i file Activeds. lib e adsiid. lib all'input del linker per il progetto.</span><span class="sxs-lookup"><span data-stu-id="bd0b6-112">Add the Activeds.lib and Adsiid.lib files to the linker input for your project.</span></span>
4.  <span data-ttu-id="bd0b6-113">Iniziare la programmazione con ADSI.</span><span class="sxs-lookup"><span data-stu-id="bd0b6-113">Begin programming with ADSI.</span></span>

<span data-ttu-id="bd0b6-114">Accedere a un dominio Windows.</span><span class="sxs-lookup"><span data-stu-id="bd0b6-114">Log on to a Windows domain.</span></span> <span data-ttu-id="bd0b6-115">È inoltre necessario disporre dell'autorizzazione per modificare i dati in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bd0b6-115">You must also have permission to modify data in Active Directory.</span></span> <span data-ttu-id="bd0b6-116">Per impostazione predefinita, l'amministratore dispone di questo privilegio.</span><span class="sxs-lookup"><span data-stu-id="bd0b6-116">By default, the Administrator has this privilege.</span></span> <span data-ttu-id="bd0b6-117">Per immettere questo esempio di codice:</span><span class="sxs-lookup"><span data-stu-id="bd0b6-117">To enter this code example:</span></span>

<span data-ttu-id="bd0b6-118">**Applicazione Visual C++ di esempio: creazione di un utente in un dominio**</span><span class="sxs-lookup"><span data-stu-id="bd0b6-118">**A Sample Visual C++ Application: Creating a User in a Domain**</span></span>

1.  <span data-ttu-id="bd0b6-119">Avviare Visual C++ 6,0.</span><span class="sxs-lookup"><span data-stu-id="bd0b6-119">Start Visual C++ 6.0.</span></span>
2.  <span data-ttu-id="bd0b6-120">Creare un progetto eseguibile autonomo.</span><span class="sxs-lookup"><span data-stu-id="bd0b6-120">Create a standalone executable project.</span></span> <span data-ttu-id="bd0b6-121">Può essere un'applicazione MFC, ATL o console.</span><span class="sxs-lookup"><span data-stu-id="bd0b6-121">It can be either an MFC, ATL, or Console Application.</span></span>
3.  <span data-ttu-id="bd0b6-122">Seguire i passaggi precedenti per configurare il progetto.</span><span class="sxs-lookup"><span data-stu-id="bd0b6-122">Follow the previous steps to set up your project.</span></span>
4.  <span data-ttu-id="bd0b6-123">Immettere l'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="bd0b6-123">Enter the following code example.</span></span> <span data-ttu-id="bd0b6-124">Sostituire la stringa "LDAP://CN = Users, DC = Fabrikam, DC = com" con il ADsPath di un contenitore nel dominio.</span><span class="sxs-lookup"><span data-stu-id="bd0b6-124">Replace the "LDAP://CN=users,DC=fabrikam,DC=com" string with the ADsPath of a container in your domain.</span></span> <span data-ttu-id="bd0b6-125">È inoltre necessario sostituire il nome utente "SergioMelchiori" con un nome utente univoco nel dominio.</span><span class="sxs-lookup"><span data-stu-id="bd0b6-125">You should also replace the user name "jeffsmith" with a user name that is unique in your domain.</span></span>

    ```C++
    #include "stdafx.h"
    #include "activeds.h"

    int main(int argc, char* argv[])
    {
        HRESULT hr;
        IADsContainer *pCont;
        IDispatch *pDisp=NULL;
        IADs *pUser;

         // Initialize COM before calling any ADSI functions or interfaces.
         CoInitialize(NULL);

        hr = ADsGetObject( L"LDAP://CN=users,DC=fabrikam,DC=com", 
                                   IID_IADsContainer, 
                                   (void**) &pCont );
        
        if ( !SUCCEEDED(hr) )
        {
            return 0;
        }

        //-----------------
        // Create a user
        //-----------------
        
        hr = pCont->Create(CComBSTR("user"), CComBSTR("cn=jeffsmith"), &pDisp );
        
        // Release the container object.    
        pCont->Release();
        
        if ( !SUCCEEDED(hr) )
        {
            return 0;
        }

        hr = pDisp->QueryInterface( IID_IADs, (void**) &pUser );

        // Release the dispatch interface.
        pDisp->Release();

        if ( !SUCCEEDED(hr) )
        {    
            return 0;
        }

        // Commit the object data to the directory.
        pUser->SetInfo();

        // Release the object.
        pUser->Release();

        CoUninitialize();
    }
    ```

    

5.  <span data-ttu-id="bd0b6-126">Compilare ed eseguire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bd0b6-126">Build and run the application.</span></span> <span data-ttu-id="bd0b6-127">Per verificare che l'utente sia stato creato, usare lo strumento di gestione Active Directory utenti e computer.</span><span class="sxs-lookup"><span data-stu-id="bd0b6-127">To verify that the user has been created, use the Active Directory Users and Computers management tool.</span></span>

 

 




