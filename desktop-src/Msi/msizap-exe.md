---
description: Msizap.exe è un'utilità della riga di comando che rimuove tutte Windows informazioni sul programma di installazione per un prodotto o tutti i prodotti installati in un computer. I prodotti installati dal programma di installazione potrebbero non funzionare dopo l'uso di Msizap.
ms.assetid: 0debb8ab-3ae7-447e-84fc-0466ec1b2f26
title: Msizap.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f29de42f41a72f06f62627489f8f44d1b21c5c76066ba1b1a990334f53c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943672"
---
# <a name="msizapexe"></a>Msizap.exe

Msizap.exe è un'utilità della riga di comando che rimuove tutte Windows informazioni sul programma di installazione per un prodotto o tutti i prodotti installati in un computer. I prodotti installati dal programma di installazione potrebbero non funzionare dopo l'uso di Msizap.

In Windows 2000 e Windows XP, sono necessari privilegi amministrativi per usare Msizap.exe.

Questo strumento è disponibile solo nei componenti [dell'SDK Windows per](platform-sdk-components-for-windows-installer-developers.md) Windows programma di installazione e non deve essere ridistribuito. Usare la versione recente di Msizap.exe (versione 3.1.4000.2726 o successiva) disponibile in Windows SDK Components for Windows Installer Developers for Windows Vista o versione successiva. Le versioni inferiori Msizap.exe possono rimuovere informazioni su tutti gli aggiornamenti applicati ad altre applicazioni nel computer dell'utente. Se queste informazioni vengono rimosse, potrebbe essere necessario rimuovere e reinstallare queste altre applicazioni per ricevere altri aggiornamenti.

## <a name="syntax"></a>Sintassi

**msizap T**_\[ WA! \] {codice prodotto}_

**msizap T**_\[ WA! \] <msi package>_

**msizap \* *** \[ WA. \]* **ALLPRODUCTS**

**msizap PWSA?!**

## <a name="command-line-options"></a>Opzioni da riga di comando

Msizap.exe le opzioni della riga di comando senza distinzione tra maiuscole e minuscole illustrate nella tabella seguente.



| Opzione | Descrizione                                                                                                                                                                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*     | Rimuove tutte le Windows del Programma di installazione e le chiavi del Registro di sistema, modifica i conteggi delle DLL condivise e arresta Windows del programma di installazione. Rimuove anche la chiave In-Progress e le informazioni di rollback.                                                                           |
| a      | Modifica solo gli ACL in Controllo completo amministratore per qualsiasi rimozione specificata.                                                                                                                                                                                            |
| g      | Per tutti gli utenti, rimuove tutti i file di dati Windows installer memorizzati nella cache che sono stati orfani.                                                                                                                                                                       |
| p      | Rimuove la In-Progress chiave.                                                                                                                                                                                                                                  |
| s      | Rimuove le informazioni di rollback.                                                                                                                                                                                                                                 |
| t      | Rimuove tutte le informazioni per il codice prodotto specificato. Quando si usa questa opzione, racchiudere il codice prodotto tra parentesi graffe. Questa opzione può essere usata con il percorso completo del file .msi o con il codice del prodotto.                                        |
| w      | Rimuove Windows informazioni sul programma di installazione per tutti gli utenti. Quando questa opzione non è impostata, vengono rimosse solo le informazioni per l'utente corrente. L'uso di questa opzione richiede che il profilo dell'utente sia caricato in modo che sia disponibile l'hive del Registro di sistema per utente dell'utente. |
| ?      | Guida dettagliata.                                                                                                                                                                                                                                                 |
| !      | Forza una risposta "sì" a qualsiasi richiesta.                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



