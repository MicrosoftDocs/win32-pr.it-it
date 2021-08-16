---
description: Specifica l'identificatore hardware PnP-X del servizio.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Elemento PnPXHardwareId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d032974486d4bd43f0a699eba6b8f6b75598c49858eeedb09bae5d3e79b11e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311516"
---
# <a name="pnpxhardwareid-element"></a>Elemento PnPXHardwareId

Specifica l'identificatore hardware PnP-X del servizio. PnP corrisponde a questo elemento con le descrizioni hardware fornite nella sezione \[ PnpxDevice \] del file INF del dispositivo. In base a queste informazioni, il servizio PnP seleziona e carica il driver di dispositivo più appropriato.

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
| [**Ospitato da**](hosted.md)<br/> | Definisce gli elementi per i servizi definiti dall'host del servizio. <br/> <br/> |



## <a name="remarks"></a>Commenti

Per specificare più ID hardware, separare gli identificatori con uno spazio, ad esempio "PnPX \_ SampleService \_ HWID \_ 1 PnPX \_ SampleService \_ HWID \_ 2 PnPX \_ SampleService1 \_ HWID \_ 3".

## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




