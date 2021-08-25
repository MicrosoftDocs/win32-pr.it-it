---
description: Vantaggi di MUI Spiegato
ms.assetid: 5b9851e0-4354-4088-b099-0f5f5fac4a35
title: Vantaggi di MUI Spiegato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971f66ef7fc094912e87d7e9ab77284fecb0931d9222e6910931b281b6308286
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829700"
---
# <a name="benefits-of-mui-explained"></a>Vantaggi di MUI Spiegato

-   [Vantaggi di MUI per gli sviluppatori](#mui-benefits-for-developers)
-   [Vantaggi di MUI per le aziende](#mui-benefits-for-enterprises)
-   [Vantaggi di MUI per gli OEM](#mui-benefits-for-oems)

## <a name="mui-benefits-for-developers"></a>Vantaggi di MUI per gli sviluppatori

Esistono molti modi possibili per implementare una soluzione MUI nelle applicazioni, ma ogni possibilità è una variante di uno dei tre metodi di base:

1.  Compilazione di un file binario (con risorse incorporate) per ogni lingua. Si tratta dello standard *di fatto per* le applicazioni legacy, in quanto si tratta del modello principale supportato dagli strumenti di sviluppo standard, ad esempio Microsoft Visual Studio. Questo modello richiede più file binari per più lingue e presenta limitazioni per quanto riguarda la distribuzione di immagini singole e scenari multilingue. Si noti che le applicazioni sviluppate con questo modello continueranno a funzionare in Windows Vista e che vengono forniti strumenti che consentono agli sviluppatori di passare da questo modello al modello più moderno descritto nel terzo metodo.
2.  Avere un file binario core indipendente dalla lingua con una libreria a collegamento dinamico (DLL) di risorse multi-linguaggio. Questo modello è sicuramente di tipo MUI, ma rende difficile aggiornare i file binari delle risorse in base alle nuove lingue. Si supponga che, oltre all'inglese, al francese e al giapponese, si voglia supportare anche il tedesco. Un intero nuovo file binario delle risorse deve essere fornito e distribuito agli utenti che potrebbero non necessariamente aver bisogno del tedesco.
3.  Avere un file binario core indipendente dalla lingua con un set di DLL di risorse per ogni lingua. Questo è il modo in cui il sistema operativo stesso viene implementato in Windows Vista e gli sviluppatori sono invitati a usare questo modello per le applicazioni perché offre più dei due modelli precedenti.

Prima della versione Windows Vista, la mancanza di supporto incorporato per quest'ultimo modello ha reso difficile l'adozione. Tuttavia, questo è cambiato e i vantaggi di questo modello sono numerosi e lo rendono un modello ideale per le applicazioni:

-   Le applicazioni possono essere rese multilingue e possono comportarsi allo stesso modo di Windows Vista, offrendo un'esperienza di lingua di visualizzazione coerente per gli utenti.
-   La flessibilità è aumentata nel rilascio di lingue aggiuntive per un'applicazione. Altri linguaggi possono essere rilasciati indipendentemente dal codice principale, il che significa che il supporto per i nuovi linguaggi può essere aggiunto nel tempo in base alle esigenze.
-   I costi si riducono durante la creazione e la manutenzione di più versioni del linguaggio.
-   Gli OEM e le aziende possono integrare facilmente le applicazioni nell'immagine del PC globalizzata, pronta per la spedizione in paesi diversi.
-   Sono disponibili strumenti e linee guida che consentono di eseguire la migrazione dell'applicazione Windows modello MUI di Vista. In particolare, MSDN fornisce un [set significativo di documentazione su](multilingual-user-interface.md) MUI.

## <a name="mui-benefits-for-enterprises"></a>Vantaggi di MUI per le aziende

MUI offre due vantaggi principali per le aziende:

-   Installazione a immagine singola: MUI consente alle aziende di implementare, supportare e gestire la stessa immagine in tutto il mondo (o in qualsiasi parte) con una singola installazione. Windows Vista estende l'implementazione a immagine singola del sistema operativo, in modo che le applicazioni aziendali possano essere distribuite anche come parte della stessa immagine.
-   Supporto per desktop multilingue: è possibile installare più Language Pack localizzati dell'interfaccia utente in un desktop, che consente a più utenti di condividere un singolo desktop continuando a usare le proprie lingue dell'interfaccia utente preferite. Questo vale anche per i computer pubblici, che necessitano di parità di trattamento per tutte le lingue parlate ufficialmente (ad esempio, in Canada e nell'Unione Europea) e per i computer condivisi per gli utenti in roaming.

## <a name="mui-benefits-for-oems"></a>Vantaggi di MUI per gli OEM

Il vantaggio principale per gli OEM è l'installazione a immagine singola abilitata da MUI, in quanto consente di creare immagini che contengono tutte le lingue necessarie per una zona geografica in modo efficace e ritardare la scelta della lingua per l'installazione iniziale del computer da parte dell'utente. In particolare, ciò consente una gestione più efficace dell'inventario per gli OEM.

Fornendo il supporto MUI per le applicazioni, Windows Vista consente anche agli OEM di fornire applicazioni a valore aggiunto nelle immagini, traendo vantaggio dall'installazione di una singola immagine, purché queste applicazioni siano abilitate per MUI.

 

 



