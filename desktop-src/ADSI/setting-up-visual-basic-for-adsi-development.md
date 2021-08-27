---
title: Configurazione di Visual Basic 6.0 per lo sviluppo ADSI
description: Questo argomento illustra come configurare Visual Basic in Visual Studio sviluppare un'applicazione ADSI.
ms.assetid: 167e89d7-80a3-4cc2-b79c-3744c1b184d6
ms.tgt_platform: multiple
keywords:
- Configurazione di Visual Basic per ADSI Development ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cadc9f74410dcb654a880920a83c20e6af9db1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885203"
---
# <a name="setting-up-visual-basic-60-for-adsi-development"></a>Configurazione di Visual Basic 6.0 per lo sviluppo ADSI

**Configurazione dell'Microsoft Visual Studio 2010 Development Environment for Visual Basic**

1.  Avviare Visual Studio 2010.
2.  Creare un nuovo Visual Basic progetto.
3.  Aggiungere un riferimento alla **libreria dei tipi DS attiva.**
    > [!Note]  
    > Se non è necessaria l'associazione anticipata di oggetti COM, ignorare questo passaggio.

     

    1.  Selezionare **Project \| Aggiungi riferimento**.
    2.  Selezionare la **scheda COM.**
    3.  Selezionare Active DS Type Library (Libreria **dei tipi DS attiva).**

4.  Iniziare a programmare con ADSI.

Prima di iniziare, accedere a un dominio Windows locale. È necessario disporre dell'autorizzazione per modificare il database di Active Directory. Per impostazione predefinita, l'amministratore dispone di questo privilegio.

**Esempio di Visual Basic 6.0: Modifica di FullName e Descrizione per un utente**

1.  Seguire i passaggi precedenti per creare un file eseguibile standard Visual Basic progetto.
2.  Fare doppio clic sul modulo . In Caricamento \_ modulo digitare quanto segue. È necessario sostituire la stringa "LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com" con l'ADsPath di un utente esistente in un contenitore nel dominio. Creare un account utente di test che può essere modificato a questo scopo.
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

    

3.  Premere **&lt; F5 &gt;** per eseguire il programma.
4.  Per verificare le modifiche, usare lo strumento Utenti e computer di Active Directory gestione dei dati. Per altre informazioni sull'uso di ADSI e Visual Basic, vedere [Accesso ad Active Directory tramite Visual Basic](accessing-active-directory-using-visual-basic.md).

 

 




