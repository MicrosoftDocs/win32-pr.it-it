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
# <a name="setting-up-visual-c-60-for-adsi-development"></a>Configurazione di Visual C++ 6,0 per lo sviluppo ADSI

Il sistema di sviluppo Microsoft Visual C++ 6,0 può essere utilizzato per sviluppare applicazioni aziendali. Per configurare l'ambiente di Visual C++ 6,0 per lo sviluppo di un'applicazione ADSI, seguire questa procedura:

**Configurazione dell'ambiente di sviluppo Microsoft Visual C++ 6,0**

1.  Puntare al Includi e alla directory della libreria. Selezionare **strumenti \| Opzioni**. Fare clic sulla scheda **directory** e specificare il percorso dei file di intestazione ADSI.
2.  Includere il file Activeds. h nel progetto.
3.  Aggiungere i file Activeds. lib e adsiid. lib all'input del linker per il progetto.
4.  Iniziare la programmazione con ADSI.

Accedere a un dominio Windows. È inoltre necessario disporre dell'autorizzazione per modificare i dati in Active Directory. Per impostazione predefinita, l'amministratore dispone di questo privilegio. Per immettere questo esempio di codice:

**Applicazione Visual C++ di esempio: creazione di un utente in un dominio**

1.  Avviare Visual C++ 6,0.
2.  Creare un progetto eseguibile autonomo. Può essere un'applicazione MFC, ATL o console.
3.  Seguire i passaggi precedenti per configurare il progetto.
4.  Immettere l'esempio di codice seguente. Sostituire la stringa "LDAP://CN = Users, DC = Fabrikam, DC = com" con il ADsPath di un contenitore nel dominio. È inoltre necessario sostituire il nome utente "SergioMelchiori" con un nome utente univoco nel dominio.

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

    

5.  Compilare ed eseguire l'applicazione. Per verificare che l'utente sia stato creato, usare lo strumento di gestione Active Directory utenti e computer.

 

 




