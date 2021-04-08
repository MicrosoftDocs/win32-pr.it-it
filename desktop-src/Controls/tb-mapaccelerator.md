---
title: Messaggio TB_MAPACCELERATOR (COMmctrl. h)
description: Determina l'ID del pulsante che corrisponde al carattere dell'acceleratore specificato.
ms.assetid: 724b593d-39af-4301-b721-0332844677b1
keywords:
- Controlli di Windows Message TB_MAPACCELERATOR
topic_type:
- apiref
api_name:
- TB_MAPACCELERATOR
- TB_MAPACCELERATORA
- TB_MAPACCELERATORW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029584d9e1614a3a135da5ebd3f4f446795fd9ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742658"
---
# <a name="tb_mapaccelerator-message"></a>TB \_ MAPACCELERATOR messaggio

Determina l'ID del pulsante che corrisponde al carattere dell'acceleratore specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Carattere del tasto di scelta rapida.

</dd> <dt>

*lParam* \[ out\]
</dt> <dd>

Puntatore a un **uint**. In caso di esito positivo, il parametro conterrà l'ID del pulsante con *wParam* come carattere di accelerazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se uno dei pulsanti presenta *wParam* come carattere dell'acceleratore oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TB \_ MAPACCELERATORW** (Unicode) e **TB \_ MAPACCELERATORA** (ANSI)<br/>       |



 

 





