---
title: Metodo ShowDefaultCharacterProperties
description: Metodo ShowDefaultCharacterProperties
ms.assetid: a3b109c0-5701-4a72-baae-bcbb97b025a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d19f92f555038fe4c13c7a752d49bf35a04b70964f6110d881976af3e72a8c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746307"
---
# <a name="showdefaultcharacterproperties-method"></a>Metodo ShowDefaultCharacterProperties

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Visualizza le proprietà del carattere predefinito.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. ShowDefaultCharacterProperties* *  \[ *X* , *Y*\]



| Parte | Descrizione                                                                                                                                                |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *X*  | facoltativo. Valore short integer che indica la coordinata orizzontale (*X* ) dello schermo per visualizzare la finestra. Questa coordinata deve essere specificata in pixel. |
| *S*  | facoltativo. Valore short integer che indica la coordinata verticale (*Y*) dello schermo per visualizzare la finestra. Questa coordinata deve essere specificata in pixel.    |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La chiamata a questo metodo consente di visualizzare la finestra delle proprietà dei caratteri predefinita (non la finestra delle proprietà di Microsoft Agent). Se non si specificano le coordinate X e Y, la finestra viene visualizzata nell'ultima posizione in cui è stata visualizzata.

## <a name="see-also"></a>Vedere anche

[**Evento DefaultCharacterChange**](defaultcharacterchange-event.md)


 

 




