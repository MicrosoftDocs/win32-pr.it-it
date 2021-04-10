---
description: Per abilitare la funzionalità del programma di installazione, un'applicazione deve chiamare una serie di funzioni durante l'inizializzazione.
ms.assetid: cfeaf9b9-f772-49f9-8b6f-e7fd0c93cc9f
title: Inizializzazione di un'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221c5d97f0febb23ba73f98605ee6ec0e853940c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227191"
---
# <a name="initializing-an-application"></a>Inizializzazione di un'applicazione

Per abilitare la funzionalità del programma di installazione, un'applicazione deve chiamare una serie di funzioni durante l'inizializzazione. Per ulteriori informazioni, vedere [meccanismo di installazione](installation-mechanism.md). Nei passaggi seguenti viene descritto come utilizzare il programma di installazione per inizializzare un'applicazione:

**Per inizializzare un'applicazione**

1.  Chiamare la funzione [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea) in modo che l'applicazione possa identificare se stessa nel programma di installazione.

    Il codice prodotto è un parametro obbligatorio per molte funzioni del programma di installazione.

2.  Chiamare la funzione [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) per raccogliere le informazioni utente alla prima avvio dell'applicazione.

    Se la chiamata a [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) ha esito negativo, chiamare la funzione [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) per raccogliere informazioni sull'utente.

3.  Se necessario, visualizzare un'interfaccia utente predefinita chiamando la funzione [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) .

    Per creare un'interfaccia utente personalizzata, registrarla con il programma di installazione chiamando la funzione [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) .

4.  Chiamare la funzione [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) per impostare il livello di registrazione.
5.  Presentare all'utente le funzionalità disponibili enumerando le funzionalità dell'applicazione. È possibile enumerare le funzionalità nei modi seguenti:
    -   Eseguire una query sul programma di installazione funzionalità per funzionalità. Ad esempio, prima che l'applicazione disegni un pulsante o una voce di menu, l'applicazione chiama la funzione [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) in modo che il programma di installazione possa verificare che la funzionalità sia disponibile.
    -   Enumerare tutte le funzionalità disponibili contemporaneamente chiamando la funzione [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) . Per usare questa funzione, l'applicazione deve chiamare ripetutamente **MsiEnumFeatures** durante l'incremento di un indice.
6.  Ottenere informazioni dettagliate sull'installazione corrente chiamando le funzioni di enumerazione seguenti ripetutamente, incrementando una variabile di indice per ogni chiamata:

    -   Chiamare la funzione [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) per enumerare i prodotti registrati con il programma di installazione.
    -   Chiamare la funzione [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) per enumerare i componenti.
    -   Chiamare la funzione [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) per enumerare i qualificatori di componente.
    -   Chiamare la funzione [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa) per enumerare i prodotti per un componente specifico.

    Se il valore restituito in una funzione di enumerazione è \_ esito positivo errore, sono ancora presenti altri elementi da enumerare e la funzione deve essere chiamata nuovamente con una variabile di indice incrementata. Se il valore restituito è errore \_ , non sono presenti \_ altri \_ elementi, tutti gli elementi sono stati enumerati e la funzione non deve essere chiamata nuovamente.

 

 



