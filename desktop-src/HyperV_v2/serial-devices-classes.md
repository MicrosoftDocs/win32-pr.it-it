---
description: I dispositivi seriali in una macchina virtuale sono costituiti da controller seriali e porte seriali. Ogni macchina virtuale ha esattamente un controller seriale e ogni controller seriale ha esattamente due porte seriali.
ms.assetid: BA24BD74-D80C-4C5C-891F-5F17CDED2EC6
title: Classi di dispositivi seriali
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b1b95a2baaf4bc3dacfddf0e18f6acd88379f958e49fc1ccbd5d6ee5cf49a11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746109"
---
# <a name="serial-devices-classes"></a>Classi di dispositivi seriali

I dispositivi seriali in una macchina virtuale sono costituiti da controller seriali e porte seriali. Ogni macchina virtuale ha esattamente un controller seriale e ogni controller seriale ha esattamente due porte seriali.

Le impostazioni per il controller seriale non sono configurabili. Pertanto, non vi è alcuna istanza di dati di impostazione associata. Inoltre, non è possibile aggiungere o rimuovere controller seriali o porte seriali da una macchina virtuale. Pertanto, non sono presenti istanze del pool di risorse per i dispositivi seriali.

Di seguito sono riportate le classi WMI di virtualizzazione correlate ai dispositivi seriali.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                      | Descrizione                                                                     |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**Msvm \_ SerialController**](msvm-serialcontroller.md)<br/>                         | Rappresenta le funzionalità e la gestione del controller seriale.<br/> |
| [**Msvm \_ SerialPort**](msvm-serialport.md)<br/>                                     | Rappresenta una porta seriale associata al controller seriale.<br/>      |
| [**Msvm \_ SerialPortOnSerialController**](msvm-serialportonserialcontroller.md)<br/> | Associa una porta seriale a un controller seriale.<br/>                   |



 

 

 




