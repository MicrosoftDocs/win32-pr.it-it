---
description: Il provider di base WMI definisce le classi che costituiscono la funzionalità principale di WMI.
ms.assetid: 6EEA4284-CCFE-4206-9EAA-B4BCF988DE03
title: Provider di base WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9927be7208d9133d65257292950913972e96483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233114"
---
# <a name="wmi-core-provider"></a>Provider di base WMI

Il provider di base WMI definisce le classi che costituiscono la funzionalità principale di WMI.

La maggior parte delle classi del provider di base WMI contiene i dati forniti dal [provider WDM](wdm-provider.md)e descrive i monitoraggi di visualizzazione. Le classi sono definite in WMI. mof e si trovano nello \\ spazio dei nomi "WMI radice".

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                           | Descrizione                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSMonitorClass**](msmonitorclass.md)<br/>                                             | è una classe di base WMI astratta. Le classi che descrivono i monitoraggi di visualizzazione video ereditano da questo [**MSMonitorClass**](msmonitorclass.md).<br/>                                                                         |
| [Classi MSMCA](msmca-classes.md)<br/>                                                   | set di classi WMI che espongono l'architettura di controllo del computer (MCA). System Abstraction Layer (SAL) fornisce tutti gli eventi segnalati nella classe MSMCA. Intel Corporation sviluppa e possiede il MCA.<br/>         |
| [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md)<br/>                         | rappresenta un contenitore per le caratteristiche di un intervallo di frequenze supportato.<br/>                                                                                                                                          |
| [**SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)<br/>     | rappresenta le funzionalità di visualizzazione supportate del monitoraggio.<br/>                                                                                                                                                           |
| [**VideoModeDescriptor**](videomodedescriptor.md)<br/>                                   | contiene gli elementi del descrittore della modalità per la matrice **MonitorSourceModes** nella classe [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md) .<br/>                                           |
| [**WMIEvent**](wmievent.md)<br/>                                                         | La classe [**WmiEvent**](wmievent.md) è una classe di base da cui derivano tutte le classi di evento WMI.<br/>                                                                                                                |
| [**WmiMonitorAnalogVideoInputParams**](wmimonitoranalogvideoinputparams.md)<br/>         | rappresenta i parametri di input video analogici di un monitor del computer.<br/>                                                                                                                                                 |
| [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md)<br/>                 | rappresenta le funzionalità di visualizzazione di base di un monitor del computer.<br/>                                                                                                                                                        |
| [**WmiMonitorBrightness**](wmimonitorbrightness.md)<br/>                                 | rappresenta i parametri di luminosità di un monitor del computer.<br/>                                                                                                                                                         |
| [**WmiMonitorBrightnessEvent**](wmimonitorbrightnessevent.md)<br/>                       | rappresenta una modifica della luminosità di un monitoraggio.<br/>                                                                                                                                                                 |
| [**WmiMonitorBrightnessMethods**](wmimonitorbrightnessmethods.md)<br/>                   | contiene i metodi che gestiscono la luminosità del monitoraggio.<br/>                                                                                                                                                                    |
| [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md)<br/>             | rappresenta le caratteristiche dei colori CIE (International Commission on illuminazione) di un monitor del computer.<br/>                                                                                                          |
| [**WmiMonitorConnectionParams**](wmimonitorconnectionparams.md)<br/>                     | contiene il tipo di connessione del monitoraggio.<br/>                                                                                                                                                                        |
| [**WmiMonitorDescriptorMethods**](wmimonitordescriptormethods.md)<br/>                   | contiene i metodi che ottengono il contenuto non elaborato della definizione del video di input dei dati di identificazione (VESA) Enhanced Extended Display Data (E-EDID) v. 1. x blocchi di dati standard a 128 byte.<br/> |
| [**WmiMonitorDigitalVideoInputParams**](wmimonitordigitalvideoinputparams.md)<br/>       | rappresenta i parametri di input per i video digitali.<br/>                                                                                                                                                                      |
| [**WmiMonitorID**](wmimonitorid.md)<br/>                                                 | rappresenta le informazioni di identificazione relative a un monitor video, ad esempio il nome del produttore, l'anno di produzione o il numero di serie.<br/>                                                                                     |
| [**WmiMonitorListedFrequencyRanges**](wmimonitorlistedfrequencyranges.md)<br/>           | elenca gli intervalli di frequenza supportati dal monitoraggio.<br/>                                                                                                                                                                |
| [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md)<br/> | elenca le modalità di origine supportate per un monitor video nel relativo descrittore di monitoraggio, se presente.<br/>                                                                                                                       |
| [**WmiMonitorRawEEdidV1Block**](wmimonitorraweedidv1block.md)<br/>                       | rappresenta i dati non elaborati di una struttura EDID (video Electronics Standard Association) migliorata.<br/>                                                                      |
| [**XYZinCIE**](xyzincie.md)<br/>                                                         | contiene le coordinate dello schermo nello spazio dei colori di International Commission on illuminazione (CIE) XYZ.<br/>                                                                                                      |



 

 

 




