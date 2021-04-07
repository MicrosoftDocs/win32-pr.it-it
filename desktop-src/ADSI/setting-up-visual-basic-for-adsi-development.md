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
# <a name="setting-up-visual-basic-60-for-adsi-development"></a>Configurazione di Visual Basic 6,0 per lo sviluppo ADSI

**Configurazione dell'ambiente di sviluppo Microsoft Visual Studio 2010 per Visual Basic**

1.  Avviare Visual Studio 2010.
2.  Creare un nuovo progetto Visual Basic.
3.  Aggiungere un riferimento alla libreria dei tipi di servizi di **dominio Active Directory**.
    > [!Note]  
    > Se non è necessaria l'associazione iniziale di oggetti COM, ignorare questo passaggio.

     

    1.  Selezionare **progetto \| Aggiungi riferimento**.
    2.  Selezionare la scheda **com** .
    3.  Selezionare **Active DS Type Library**.

4.  Iniziare la programmazione con ADSI.

Prima di iniziare, accedere a un dominio Windows. È necessario disporre dell'autorizzazione per modificare il database di Active Directory. Per impostazione predefinita, l'amministratore dispone di questo privilegio.

**Applicazione Visual Basic 6,0 di esempio: modifica di FullName e Description per un utente**

1.  Seguire i passaggi precedenti per creare un progetto di Visual Basic eseguibile standard.
2.  Fare doppio clic sul form. In \_ caricamento del modulo digitare quanto segue. È necessario sostituire la stringa "LDAP://CN = SergioMelchiori, CN = Users, DC = Fabrikam, DC = com" con ADsPath di un utente esistente in un contenitore del dominio. Creare un account utente di test che può essere modificato a questo scopo.
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

    

3.  Premere **<F5>** per eseguire il programma.
4.  Per verificare le modifiche, usare lo strumento di gestione Active Directory utenti e computer. Per ulteriori informazioni sull'utilizzo di ADSI e Visual Basic, vedere [accesso Active Directory utilizzando Visual Basic](accessing-active-directory-using-visual-basic.md).

 

 




