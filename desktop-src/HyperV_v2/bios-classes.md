---
description: Il BIOS virtuale è un'immagine software caricata nella RAM per configurare alcuni degli aspetti di base di e avviare un computer. Esiste un elemento BIOS per ogni computer e tale elemento non può essere sostituito o rimosso.
ms.assetid: EC691401-947F-4B56-A8A7-F0ECBF01677B
title: Classi BIOS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9605f28a23fc84b653ba5efe6c6e4be057eba48da81ddb777c7516d1317da6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813638"
---
# <a name="bios-classes"></a>Classi BIOS

Il BIOS virtuale è un'immagine software caricata nella RAM per configurare alcuni degli aspetti di base di e avviare un computer. Esiste un elemento BIOS per ogni computer e tale elemento non può essere sostituito o rimosso. Non è quindi disponibile alcun pool di risorse per l'aggiunta di nuovi elementi BIOS alla macchina virtuale. Anche l'elemento BIOS non dispone di una propria classe SettingData per descrivere le impostazioni per il BIOS. Impostazioni per il BIOS, ad esempio i numeri di serie, l'ordine di avvio e lo stato di blocco num, sono disponibili nella [**classe Msvm \_ VirtualSystemSettingData.**](msvm-virtualsystemsettingdata.md)

Di seguito sono riportate le classi WMI di virtualizzazione correlate al BIOS. Queste classi sono in \\ \\ . \\ Spazio \\ dei nomi di virtualizzazione radice.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                    | Descrizione                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**Msvm \_ BIOSElement**](msvm-bioselement.md)<br/> | Rappresenta il software di basso livello caricato nella RAM per configurare e avviare il sistema.<br/> |
| [**Msvm \_ SystemBIOS**](msvm-systembios.md)<br/>   | Usato per associare una macchina virtuale al RELATIVO BIOS.<br/>                                           |



 

 

 




