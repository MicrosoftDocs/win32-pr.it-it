---
title: Ripristino configurazione di sistema
description: Imposta i punti di ripristino del sistema e monitora le modifiche del sistema chiave da un programma per consentire il rollback del sistema a uno stato precedente. Scrivere codice di ripristino automatico o script WMI per ripristinare lo stato del sistema in un punto di ripristino registrato.
ms.assetid: 6861eedc-2bd9-49c7-8682-ea557fa29d28
keywords:
- Ripristino configurazione di sistema
- Ripristino configurazione di sistema, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bdc4555171ad867f6e6b925144d9ed673ffc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118043"
---
# <a name="system-restore"></a>Ripristino configurazione di sistema

## <a name="purpose"></a>Scopo

Ripristino configurazione di sistema monitora e registra automaticamente le modifiche di sistema principali nel computer di un utente. È progettato per ridurre i costi di supporto e aumentare la soddisfazione dei clienti consentendo a un utente di annullare una modifica che potrebbe avere causato un problema con il sistema o ripristinare un giorno in cui il sistema è stato in grado di garantire prestazioni ottimali.

> [!Note]  
> La seguente documentazione è destinata agli sviluppatori. Per informazioni sull'utilizzo di ripristino configurazione di sistema da parte dell'utente finale, vedere [che cos'è ripristino configurazione di sistema?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)

 

## <a name="developer-audience"></a>Sviluppatori

L'API di ripristino del sistema è progettata per l'uso da parte dei programmatori C/C++. Per utilizzare l'interfaccia di scripting, è necessaria una certa familiarità con Strumentazione gestione Windows (WMI).

## <a name="run-time-requirements"></a>Requisiti di runtime

L'API ripristino di sistema è supportata nei sistemi operativi client a partire da Windows XP. Per informazioni sui sistemi operativi necessari per usare un particolare elemento API, vedere la sezione requisiti della relativa documentazione.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                | Descrizione                                                                    |
|------------------------------------------------------|--------------------------------------------------------------------------------|
| [Overview](about-system-restore.md)<br/>      | Panoramica del funzionamento del ripristino del sistema.<br/>                            |
| [Riferimento](system-restore-reference.md)<br/> | Documentazione delle funzioni, delle strutture e delle classi di ripristino del sistema.<br/> |
| [Esempi](using-system-restore.md)<br/>       | Programma di esempio scritto in C.<br/>                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[WMI](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

