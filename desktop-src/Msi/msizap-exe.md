---
description: Msizap.exe è un'utilità della riga di comando che rimuove tutte le informazioni Windows Installer per un prodotto o tutti i prodotti installati in un computer. I prodotti installati dal programma di installazione potrebbero non funzionare dopo l'uso di Msizap.
ms.assetid: 0debb8ab-3ae7-447e-84fc-0466ec1b2f26
title: Msizap.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a89f2287443bc442ee767b01e975d6bcc118c1d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049828"
---
# <a name="msizapexe"></a>Msizap.exe

Msizap.exe è un'utilità della riga di comando che rimuove tutte le informazioni Windows Installer per un prodotto o tutti i prodotti installati in un computer. I prodotti installati dal programma di installazione potrebbero non funzionare dopo l'uso di Msizap.

In Windows 2000 e Windows XP sono necessari privilegi amministrativi per usare Msizap.exe.

Questo strumento è disponibile solo nei [componenti Windows SDK per gli sviluppatori di Windows Installer](platform-sdk-components-for-windows-installer-developers.md) e non deve essere ridistribuito. Utilizzare la versione recente di Msizap.exe (versione 3.1.4000.2726 o successiva) disponibile nei componenti Windows SDK per Windows Installer sviluppatori per Windows Vista o versione successiva. Versioni minori di Msizap.exe possono rimuovere informazioni su tutti gli aggiornamenti applicati ad altre applicazioni nel computer dell'utente. Se queste informazioni vengono rimosse, potrebbe essere necessario rimuovere e reinstallare le altre applicazioni per ricevere ulteriori aggiornamenti.

## <a name="syntax"></a>Sintassi

**Msizap T**_\[ WA! \] {Codice prodotto}_

**Msizap T**_\[ WA! \] <msi package>_

**\* *** Msizap \[ WA! \]* **ALLPRODUCTS**

**Msizap PWSA?**

## <a name="command-line-options"></a>Opzioni da riga di comando

Msizap.exe usa le opzioni della riga di comando senza distinzione tra maiuscole e minuscole mostrate nella tabella seguente.



| Opzione | Descrizione                                                                                                                                                                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*     | Rimuove tutti i Windows Installer cartelle e le chiavi del registro di sistema, regola i conteggi delle DLL condivise e arresta Windows Installer servizio. Rimuove anche la chiave di In-Progress e le informazioni di rollback.                                                                           |
| a      | Modifica solo gli ACL per il controllo completo dell'amministratore per qualsiasi rimozione specificata.                                                                                                                                                                                            |
| g      | Per tutti gli utenti, rimuove tutti i file di dati Windows Installer memorizzati nella cache che sono stati orfani.                                                                                                                                                                       |
| p      | Rimuove la chiave In-Progress.                                                                                                                                                                                                                                  |
| s      | Rimuove le informazioni di rollback.                                                                                                                                                                                                                                 |
| u      | Rimuove tutte le informazioni per il codice prodotto specificato. Quando si usa questa opzione, racchiudere il codice del prodotto tra parentesi graffe. Questa opzione può essere utilizzata con il percorso completo del file con estensione msi o con il codice prodotto.                                        |
| w      | Rimuove Windows Installer informazioni per tutti gli utenti. Quando questa opzione non è impostata, vengono rimosse solo le informazioni relative all'utente corrente. Per usare questa opzione è necessario che il profilo dell'utente sia caricato in modo che l'hive del registro di sistema per utente sia disponibile. |
| ?      | Guida dettagliata.                                                                                                                                                                                                                                                 |
| !      | Forza una risposta "Yes" a qualsiasi richiesta.                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



