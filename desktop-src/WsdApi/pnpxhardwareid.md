---
description: Specifica l'identificatore hardware PnP-X del servizio.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Elemento PnPXHardwareId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55e5e38b669a289545225df96fad05e55069b474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310283"
---
# <a name="pnpxhardwareid-element"></a>Elemento PnPXHardwareId

Specifica l'identificatore hardware PnP-X del servizio. PnP corrisponde a questo elemento con le descrizioni hardware fornite nella \[ \] sezione PnpxDevice del file inf del dispositivo. In base a queste informazioni, il servizio PnP seleziona e carica il driver di dispositivo più appropriato.

## <a name="usage"></a>Utilizzo

``` syntax
<PnPXHardwareId/>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                             | Descrizione                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [**ospitato**](hosted.md)<br/> | Definisce gli elementi per i servizi definiti dall'host del servizio. <br/> <br/> |



## <a name="remarks"></a>Commenti

Per specificare più di un ID hardware, separare gli identificatori con uno spazio, ad esempio, "PnPX \_ SampleService \_ HWID \_ 1 PnPX \_ SampleService \_ HWID \_ 2 PnPX SampleService1 \_ \_ HWID \_ 3".

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




