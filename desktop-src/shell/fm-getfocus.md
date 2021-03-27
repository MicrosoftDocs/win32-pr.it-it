---
description: Inviato da un'estensione di file Manager per recuperare il tipo di finestra di file Manager con lo stato attivo per l'input.
title: Messaggio FM_GETFOCUS (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFOCUS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: e2d5f825-5678-4dd7-adad-eec1cbcc7e49
ms.openlocfilehash: af6e0894b3734f976302eacbf0575a017f054f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979735"
---
# <a name="fm_getfocus-message"></a>\_Messaggio FM GETfocus

Inviato da un'estensione di file Manager per recuperare il tipo di finestra di file Manager con lo stato attivo per l'input.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il tipo di finestra di file Manager con lo stato attivo per l'input. Può essere uno dei valori seguenti.



| Codice restituito                                                                                    | Descrizione                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_dir FMFOCUS**</dt> </dl>    | Parte della directory di una finestra di directory.<br/> |
| <dl> <dt>**\_albero FMFOCUS**</dt> </dl>   | Parte albero di una finestra di directory.<br/>      |
| <dl> <dt>**\_unità FMFOCUS**</dt> </dl> | Barra di unità di una finestra di directory.<br/>         |
| <dl> <dt>**\_ricerca FMFOCUS**</dt> </dl> | Finestra Risultati ricerca.<br/>                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



 

 




