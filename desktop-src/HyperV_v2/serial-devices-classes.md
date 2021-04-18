---
description: I dispositivi seriali in una macchina virtuale sono costituiti da controller seriali e porte seriali. Ogni macchina virtuale ha esattamente un controller seriale e ogni controller seriale ha esattamente due porte seriali.
ms.assetid: BA24BD74-D80C-4C5C-891F-5F17CDED2EC6
title: Classi di dispositivi seriali
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ae796b86837372d60bba83e51e0190b9c7d3f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313837"
---
# <a name="serial-devices-classes"></a>Classi di dispositivi seriali

I dispositivi seriali in una macchina virtuale sono costituiti da controller seriali e porte seriali. Ogni macchina virtuale ha esattamente un controller seriale e ogni controller seriale ha esattamente due porte seriali.

Le impostazioni per il controller seriale non sono configurabili; Pertanto, non è associata alcuna istanza di dati di impostazione. Inoltre, non è possibile aggiungere o rimuovere controller seriali o porte seriali da una macchina virtuale. Non sono pertanto disponibili istanze del pool di risorse per i dispositivi seriali.

Di seguito sono riportate le classi WMI di virtualizzazione correlate ai dispositivi seriali.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                      | Descrizione                                                                     |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_Controller seriale MSVM**](msvm-serialcontroller.md)<br/>                         | Rappresenta le funzionalità e la gestione del controller seriale.<br/> |
| [**MSVM \_ SerialPort**](msvm-serialport.md)<br/>                                     | Rappresenta una porta seriale associata al controller seriale.<br/>      |
| [**\_SerialPortOnSerialController MSVM**](msvm-serialportonserialcontroller.md)<br/> | Associa una porta seriale a un controller seriale.<br/>                   |



 

 

 




