---
title: Ripristino configurazione di sistema
description: Imposta i punti di ripristino del sistema e monitora le modifiche principali del sistema da un programma per consentire il rollback del sistema a uno stato precedente. Scrivere codice di ripristino automatico o script WMI per ripristinare lo stato del sistema in un punto di ripristino registrato.
ms.assetid: 6861eedc-2bd9-49c7-8682-ea557fa29d28
keywords:
- Ripristino configurazione di sistema
- Ripristino configurazione di sistema, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4472806aa2c0b6f8a29cc4e687d16e262639a66c65bda37fdca970c6c38b656f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111291"
---
# <a name="system-restore"></a>Ripristino configurazione di sistema

## <a name="purpose"></a>Scopo

Ripristino configurazione di sistema monitora e registra automaticamente le modifiche principali del sistema nel computer di un utente. È progettato per ridurre i costi di supporto e aumentare la soddisfazione dei clienti consentendo a un utente di annullare una modifica che potrebbe aver causato un problema con il sistema o ripristinare un giorno in cui le prestazioni del sistema erano ottimali.

> [!Note]  
> La documentazione seguente è destinata agli sviluppatori. Se si è un utente finale che cerca informazioni su come usare Ripristino configurazione di sistema, vedere [Informazioni Ripristino configurazione di sistema?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)

 

## <a name="developer-audience"></a>Sviluppatori

L Ripristino configurazione di sistema'API è progettata per l'uso da parte dei programmatori C/C++. Per usare l'interfaccia di scripting, è necessaria una familiarità con Windows Management Instrumentation (WMI).

## <a name="run-time-requirements"></a>Requisiti di runtime

L'API Ripristino configurazione di sistema è supportata nei sistemi operativi client a partire da Windows XP. Per informazioni sui sistemi operativi necessari per usare un particolare elemento API, vedere la sezione Requisiti della relativa documentazione.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                | Descrizione                                                                    |
|------------------------------------------------------|--------------------------------------------------------------------------------|
| [Overview](about-system-restore.md)<br/>      | Panoramica del funzionamento Ripristino configurazione di sistema.<br/>                            |
| [Riferimento](system-restore-reference.md)<br/> | Documentazione di Ripristino configurazione di sistema funzioni, strutture e classi.<br/> |
| [Esempi](using-system-restore.md)<br/>       | Programma di esempio scritto in C.<br/>                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[WMI](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

