---
description: Quando si imposta un livello di autenticazione per un'applicazione, si determina il livello di autenticazione eseguito quando i client chiamano l'applicazione.
ms.assetid: a59935de-6b8f-4c0a-8479-e30bc0509698
title: Impostazione di un livello di autenticazione per un'applicazione server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6248574117a55420940fbaf24f88c5d3b2c8721e6fa022bad5923ba658bf5da7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546255"
---
# <a name="setting-an-authentication-level-for-a-server-application"></a>Impostazione di un livello di autenticazione per un'applicazione server

Quando si imposta un livello di autenticazione per un'applicazione, si determina il livello di autenticazione eseguito quando i client chiamano l'applicazione. Livelli di autenticazione più elevati offrono maggiore sicurezza e integrità dei dati, anche se in genere con una riduzione delle prestazioni. Per altre informazioni, vedere [Autenticazione client.](client-authentication.md)

**Per selezionare un livello di autenticazione per un'applicazione server**

1.  Fare clic con il pulsante destro del mouse sull'applicazione COM+ per cui si sta impostando l'autenticazione, quindi **scegliere Proprietà.**

2.  Nella finestra di dialogo delle proprietà dell'applicazione fare clic **sulla scheda** Sicurezza .

3.  Nella casella **Livello di autenticazione per** le chiamate selezionare il livello appropriato. I livelli sono i seguenti, ordinati dal livello di sicurezza più basso al più alto:

    -   **Nessuno**. Non viene eseguita alcuna autenticazione.
    -   **Connessione**. Autentica le credenziali solo quando viene eseguita la connessione.
    -   **Chiamare**. Autentica le credenziali all'inizio di ciascuna chiamata.
    -   **Pacchetto**. Autentica le credenziali e verifica la ricezione di tutti i dati della chiamata. Questa è l'impostazione predefinita per le applicazioni server COM+.
    -   **Integrità dei pacchetti**. Autentica le credenziali e verifica che nessuna chiamata di dati sia stata modificata durante il passaggio.
    -   **Privacy dei pacchetti.** Autentica le credenziali e codifica il pacchetto, includendo i dati e l'identità e la firma del mittente.

4.  Fare clic su **OK**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Abilitazione dell'autenticazione per un'applicazione di libreria](enabling-authentication-for-a-library-application.md)
</dt> </dl>

 

 



