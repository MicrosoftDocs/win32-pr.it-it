---
description: Specifica l'identificatore hardware PnP-X del servizio.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Elemento PnPXHardwareId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0ffc389ca6df363439dd6463b3f86ca756359e8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996528"
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



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




