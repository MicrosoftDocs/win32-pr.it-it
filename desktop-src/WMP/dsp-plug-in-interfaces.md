---
title: Interfacce plug-in DSP
description: Interfacce plug-in DSP
ms.assetid: 4660f928-2e92-468f-9e2b-b411931dfded
keywords:
- Windows Media Player plug-in, interfacce DSP
- Windows Media Player plug-in, interfacce
- plug-in, interfacce DSP
- plug-in, interfacce
- plug-in per l'elaborazione di segnali digitali, interfacce
- plug-in di elaborazione del segnale digitale,interfaccia ISpecifyPropertyPage
- plug-in DSP, interfacce
- Plug-in DSP,interfaccia ISpecifyPropertyPage
- interfacce, plug-in DSP
- ISpecifyPropertyPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3bd030b09377adfe965698d6c411f1a39a745979f2db2eae9f0c613cad843d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863371"
---
# <a name="dsp-plug-in-interfaces"></a>Interfacce plug-in DSP

Le interfacce plug-in DSP (Digital Signal Processing) vengono usate per gestire il trasferimento dei dati tra Windows Media Player e il plug-in. Tutti i plug-in DSP possono implementare facoltativamente **l'interfaccia ISpecifyPropertyPage** per fornire un'implementazione della pagina delle proprietà.

Le interfacce seguenti sono necessarie per la creazione di plug-in DSP.



| Interfaccia                                                | Descrizione                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IMediaObject**                                         | Gestisce lo scambio di dati con Windows Media Player ed esegue attività di elaborazione dei segnali digitali. La documentazione dettagliata è inclusa in DirectX SDK. |
| [IWMPMediaPluginRegistrar](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar) | Gestisce la registrazione del plug-in.                                                                                                                          |
| [IWMPPlugin](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin)                             | Gestisce la connessione a Windows Media Player.                                                                                                        |
| [IWMPPluginEnable](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmppluginenable)                 | Archivia se il plug-in è attualmente abilitato da Windows Media Player.                                                                               |
| [IWMPServices](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices)                         | Recupera informazioni dal lettore sull'ora e sullo stato del flusso corrente.                                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sulla programmazione di plug-in DSP**](dsp-plug-ins-programming-reference.md)
</dt> </dl>

 

 




