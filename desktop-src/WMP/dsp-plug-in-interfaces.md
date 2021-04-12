---
title: Interfacce plug-in DSP
description: Interfacce plug-in DSP
ms.assetid: 4660f928-2e92-468f-9e2b-b411931dfded
keywords:
- Plug-in di Windows Media Player, interfacce DSP
- Plug-in di Windows Media Player, interfacce
- plug-in, interfacce DSP
- plug-in, interfacce
- plug-in di elaborazione dei segnali digitali, interfacce
- plug-in per l'elaborazione di segnali digitali, interfaccia ISpecifyPropertyPage
- Plug-in DSP, interfacce
- Plug-in DSP, interfaccia ISpecifyPropertyPage
- interfacce, plug-in DSP
- ISpecifyPropertyPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ab945b24f8646d986ab7d5d44e12ef3249d
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "104398744"
---
# <a name="dsp-plug-in-interfaces"></a>Interfacce plug-in DSP

Le interfacce del plug-in DSP (Digital Signal Processing) vengono utilizzate per gestire il trasferimento dei dati tra Windows Media Player e il plug-in. Tutti i plug-in DSP possono implementare facoltativamente l'interfaccia **ISpecifyPropertyPage** per fornire un'implementazione della pagina delle proprietà.

Per la creazione di plug-in DSP sono necessarie le interfacce seguenti.



| Interfaccia                                                | Descrizione                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IMediaObject**                                         | Gestisce lo scambio di dati con Windows Media Player ed esegue attività di elaborazione di segnali digitali. La documentazione dettagliata è inclusa in DirectX SDK. |
| [IWMPMediaPluginRegistrar](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar) | Gestisce la registrazione del plug-in.                                                                                                                          |
| [IWMPPlugin](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin)                             | Gestisce la connessione a Windows Media Player.                                                                                                        |
| [IWMPPluginEnable](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmppluginenable)                 | Archivia se il plug-in è attualmente abilitato da Windows Media Player.                                                                               |
| [IWMPServices](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices)                         | Recupera le informazioni dal lettore sull'ora del flusso corrente e sullo stato del flusso.                                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione di plug-in DSP**](dsp-plug-ins-programming-reference.md)
</dt> </dl>

 

 




