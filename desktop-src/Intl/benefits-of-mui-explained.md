---
description: Vantaggi di MUI
ms.assetid: 5b9851e0-4354-4088-b099-0f5f5fac4a35
title: Vantaggi di MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1915e58e28ac9c7b3a43cc0ba217b8d56657c1b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049449"
---
# <a name="benefits-of-mui-explained"></a>Vantaggi di MUI

-   [Vantaggi di MUI per gli sviluppatori](#mui-benefits-for-developers)
-   [Vantaggi MUI per le aziende](#mui-benefits-for-enterprises)
-   [Vantaggi MUI per gli OEM](#mui-benefits-for-oems)

## <a name="mui-benefits-for-developers"></a>Vantaggi di MUI per gli sviluppatori

Esistono molti modi possibili per implementare una soluzione MUI nelle applicazioni, ma ogni possibilità è una variante di uno dei tre metodi di base seguenti:

1.  Compilazione di un file binario (con risorse predefinite) per ogni lingua. Si tratta dello standard *de facto* per le applicazioni legacy, poiché si tratta del modello primario supportato dagli strumenti di sviluppo standard, ad esempio Microsoft Visual Studio. Questo modello richiede più file binari per più lingue e presenta limitazioni per quanto riguarda la distribuzione di un'immagine singola e gli scenari multilingue. Si noti che le applicazioni sviluppate con questo modello continueranno a funzionare in Windows Vista e che gli strumenti forniti consentono agli sviluppatori di passare da questo modello al modello più moderno descritto nel terzo metodo.
2.  Avere un file binario Core indipendente dalla lingua con una libreria di collegamento dinamico (DLL) di risorse multilingue. Questo modello è certamente intuitivo, ma rende difficile aggiornare i file binari delle risorse per adattarli a nuove lingue. Si supponga che, oltre all'inglese, francese e giapponese, si voglia supportare anche il tedesco. È necessario fornire e distribuire un file binario di risorse completamente nuovo per gli utenti che potrebbero non avere necessariamente il tedesco.
3.  Avere un file binario Core indipendente dalla lingua con un set di dll di risorse per ogni lingua. Questo è il modo in cui il sistema operativo stesso viene implementato in Windows Vista e gli sviluppatori sono invitati a utilizzare questo modello per le applicazioni, in quanto offre oltre i due modelli precedenti.

Prima della versione di Windows Vista, la mancanza di supporto incorporato per questo secondo modello rendeva difficile l'adozione. Tuttavia, questo è stato modificato e i vantaggi di questo modello sono numerosi e costituiscono un ottimo modello per le applicazioni:

-   Le applicazioni possono essere rese multilingue e possono comportarsi in modo analogo a Windows Vista, offrendo un'esperienza di linguaggio di visualizzazione coerente per gli utenti.
-   La flessibilità è aumentata nel rilascio di lingue aggiuntive per un'applicazione. Le lingue aggiuntive possono essere rilasciate indipendentemente dal codice principale, il che significa che è possibile aggiungere il supporto per nuove lingue nel tempo in base alle esigenze.
-   Il costo viene ridotto durante la creazione e la manutenzione di più versioni linguistiche.
-   Gli OEM e le aziende possono integrare facilmente le applicazioni nell'immagine del PC globalizzato, pronti per la spedizione in paesi diversi.
-   Sono disponibili strumenti e linee guida che consentono di eseguire la migrazione dell'applicazione al modello MUI di Windows Vista. In particolare, MSDN fornisce un [set di documentazione significativo](multilingual-user-interface.md) su MUI.

## <a name="mui-benefits-for-enterprises"></a>Vantaggi MUI per le aziende

MUI offre due vantaggi principali per le aziende:

-   Installazione di un'immagine singola: MUI consente alle aziende di implementare, supportare e mantenere le stesse immagini di tutto il mondo (o parte di essa) con un'unica installazione. Windows Vista estende l'implementazione di un'unica immagine del sistema operativo, in modo che le applicazioni aziendali possano essere distribuite anche come parte della stessa immagine.
-   Supporto per desktop multilingue: è possibile installare più Language Pack localizzati dell'interfaccia utente su un desktop, in modo da consentire a più utenti di condividere un singolo desktop continuando a usare le proprie lingue dell'interfaccia utente preferite. Questo vale anche per i computer pubblici, che richiedono lo stesso trattamento per tutte le lingue ufficialmente pronunciate, ad esempio in Canada e nell'Unione europea, e per i computer condivisi per gli utenti mobili.

## <a name="mui-benefits-for-oems"></a>Vantaggi MUI per gli OEM

Il vantaggio principale per gli OEM è la singola installazione di immagini abilitata da MUI, in quanto consente di creare immagini che contengono tutte le lingue necessarie per indirizzare una zona geografica in modo efficace e di ritardare la scelta della lingua per l'installazione iniziale del computer da parte dell'utente. In particolare, ciò consente una gestione più efficace dell'inventario per gli OEM.

Grazie al supporto MUI per le applicazioni, Windows Vista consente agli OEM di fornire applicazioni a valore aggiunto sulle proprie immagini, sfruttando al contempo l'installazione di una singola immagine, purché queste applicazioni siano abilitate per MUI.

 

 



