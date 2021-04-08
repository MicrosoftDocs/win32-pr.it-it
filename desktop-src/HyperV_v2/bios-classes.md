---
description: Il BIOS virtuale è un'immagine software caricata in RAM per configurare alcuni degli aspetti di base di e avviare un sistema di computer. È presente un solo elemento BIOS per computer e tale elemento non può essere sostituito o rimosso.
ms.assetid: EC691401-947F-4B56-A8A7-F0ECBF01677B
title: Classi BIOS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e725910bbeb1032f876b5e4fcf08da4a6ea60bc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967556"
---
# <a name="bios-classes"></a>Classi BIOS

Il BIOS virtuale è un'immagine software caricata in RAM per configurare alcuni degli aspetti di base di e avviare un sistema di computer. È presente un solo elemento BIOS per computer e tale elemento non può essere sostituito o rimosso. Non è quindi disponibile alcun pool di risorse per l'aggiunta di nuovi elementi BIOS alla macchina virtuale. L'elemento BIOS non dispone inoltre di una propria classe SettingData per descrivere le impostazioni per il BIOS. Le impostazioni per il BIOS, ad esempio i numeri di serie, l'ordine di avvio e lo stato di blocco num, si trovano nella classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) .

Di seguito sono riportate le classi WMI di virtualizzazione correlate al BIOS. Queste classi si trovano in \\ \\ . \\ \\Spazio dei nomi di virtualizzazione radice.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                    | Descrizione                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**MSVM \_ bioselement**](msvm-bioselement.md)<br/> | Rappresenta il software di basso livello caricato in RAM per configurare e avviare il sistema.<br/> |
| [**\_SystemBIOS MSVM**](msvm-systembios.md)<br/>   | Utilizzato per associare una macchina virtuale al relativo BIOS.<br/>                                           |



 

 

 




