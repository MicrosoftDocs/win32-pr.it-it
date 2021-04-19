---
description: Quando si imposta un livello di autenticazione per un'applicazione, è necessario determinare il grado di autenticazione eseguito quando i client eseguono chiamate nell'applicazione.
ms.assetid: a59935de-6b8f-4c0a-8479-e30bc0509698
title: Impostazione di un livello di autenticazione per un'applicazione server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83450b3f8d1939d08cc3d16a21f438c8da6f8fc1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304937"
---
# <a name="setting-an-authentication-level-for-a-server-application"></a>Impostazione di un livello di autenticazione per un'applicazione server

Quando si imposta un livello di autenticazione per un'applicazione, è necessario determinare il grado di autenticazione eseguito quando i client eseguono chiamate nell'applicazione. Livelli di autenticazione più elevati offrono maggiore sicurezza e integrità dei dati, anche se in genere si verifica un calo delle prestazioni. Per ulteriori informazioni, vedere [autenticazione client](client-authentication.md).

**Per selezionare un livello di autenticazione per un'applicazione server**

1.  Fare clic con il pulsante destro del mouse sull'applicazione COM+ per cui si sta impostando l'autenticazione, quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo Proprietà applicazione fare clic sulla scheda **sicurezza** .

3.  Nella casella **livello di autenticazione per le chiamate** selezionare il livello appropriato. I livelli sono i seguenti, ordinati dalla sicurezza più bassa alla più alta:

    -   **Nessuno**. Non viene eseguita alcuna autenticazione.
    -   **Connettersi**. Autentica le credenziali solo quando viene eseguita la connessione.
    -   **Chiamare**. Autentica le credenziali all'inizio di ciascuna chiamata.
    -   **Pacchetto**. Autentica le credenziali e verifica la ricezione di tutti i dati della chiamata. Si tratta dell'impostazione predefinita per le applicazioni server COM+.
    -   **Integrità dei pacchetti**. Autentica le credenziali e verifica che nessuna chiamata di dati sia stata modificata durante il passaggio.
    -   **Privacy del pacchetto**. Autentica le credenziali e codifica il pacchetto, includendo i dati e l'identità e la firma del mittente.

4.  Fare clic su **OK**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Abilitazione dell'autenticazione per un'applicazione di libreria](enabling-authentication-for-a-library-application.md)
</dt> </dl>

 

 



