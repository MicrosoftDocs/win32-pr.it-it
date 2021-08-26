---
description: Consente al callback di aggiungere elementi nella parte inferiore del menu esteso.
title: DFM_MERGECONTEXTMENU_BOTTOM messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 37414335-4f3c-461e-bd05-d6ef850f972a
api_name:
- DFM_MERGECONTEXTMENU_BOTTOM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 11dade0f4b9526fa3c384f612b2c23eb77b437ef361d16c2adffc0a49df2ca28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111841"
---
# <a name="dfm_mergecontextmenu_bottom-message"></a>Messaggio DFM \_ MERGECONTEXTMENU \_ BOTTOM

Consente al callback di aggiungere elementi nella parte inferiore del menu esteso.


```C++
DFM_MERGECONTEXTMENU_BOTTOM

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pqcminfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) contenente le informazioni utilizzate nell'unione.

</dd> <dt>

*Flag uFlags* \[ Pollici\]
</dt> <dd>

Flag che specificano come è possibile modificare il menu di scelta rapida. Questo parametro usa i valori CMF \_ \* descritti in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).

</dd> </dl>

## <a name="remarks"></a>Commenti

Se gli elementi vengono aggiunti al menu di scelta rapida esteso, devono essere supportati con routine che rispondono in modo appropriato quando uno di tali elementi viene richiamato tramite [**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md).

Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda di come viene costruito l'oggetto del menu di scelta rapida predefinito. Per la costruzione sono disponibili due API, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX è**](dfm-invokecommandex.md) una versione estesa di questo messaggio e fornisce ulteriori informazioni al callback. Usare **DFM \_ INVOKECOMMANDEX** se le informazioni aggiuntive fornite da tale interfaccia sono necessarie nell'implementazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




