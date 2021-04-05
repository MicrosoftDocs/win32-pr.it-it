---
title: Metodo ShowDefaultCharacterProperties
description: Metodo ShowDefaultCharacterProperties
ms.assetid: a3b109c0-5701-4a72-baae-bcbb97b025a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f055b2ca0f00e0a13c24ec95dc82509ae9c45b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709913"
---
# <a name="showdefaultcharacterproperties-method"></a>Metodo ShowDefaultCharacterProperties

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Consente di visualizzare le proprietà del carattere predefinito.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente * * *. ShowDefaultCharacterProperties* *  \[ *X* , *Y*\]



| Parte | Descrizione                                                                                                                                                |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *X*  | facoltativo. Valore short integer che indica la coordinata orizzontale (*X* ) dello schermo per visualizzare la finestra. Questa coordinata deve essere specificata in pixel. |
| *S*  | facoltativo. Valore short integer che indica la coordinata verticale (*Y*) dello schermo per visualizzare la finestra. Questa coordinata deve essere specificata in pixel.    |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La chiamata a questo metodo consente di visualizzare la finestra Proprietà carattere predefinita (non la finestra delle proprietà dell'agente Microsoft). Se non si specificano le coordinate X e Y, la finestra viene visualizzata nell'ultima posizione in cui è stata visualizzata.

## <a name="see-also"></a>Vedere anche

[**Evento DefaultCharacterChange**](defaultcharacterchange-event.md)


 

 




