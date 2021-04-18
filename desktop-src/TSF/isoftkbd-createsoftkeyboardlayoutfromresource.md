---
title: Metodo ISoftKbd CreateSoftKeyboardLayoutFromResource (Softkbdc. h)
description: Il metodo ISoftKbd CreateSoftKeybboardLayoutFromResource crea un layout di tastiera soft dalla risorsa specificata.
ms.assetid: c1b2f8bd-8065-426d-9c23-67fa46a33dc8
keywords:
- Framework servizi di testo Metodo CreateSoftKeyboardLayoutFromResource
- Framework dei servizi di testo del metodo CreateSoftKeyboardLayoutFromResource, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo CreateSoftKeyboardLayoutFromResource
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromResource
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f454b5d8f3366517d91170d6a92d6a9dbed5764
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302103"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromresource-method"></a>Metodo ISoftKbd:: CreateSoftKeyboardLayoutFromResource

Il metodo **ISoftKbd:: CreateSoftKeybboardLayoutFromResource** crea un layout di tastiera soft dalla risorsa specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateSoftKeyboardLayoutFromResource(
  [in]  WCHAR *lpszResFile,
  [in]  WCHAR *lpszResType,
  [in]  WCHAR *lpszXMLResString,
  [out] DWORD *lpdwLayoutCookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszResFile* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione zero che indica il nome del file di risorse.

</dd> <dt>

*lpszResType* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione zero che indica il tipo di risorsa.

</dd> <dt>

*lpszXMLResString* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione zero che identifica la risorsa.

</dd> <dt>

*lpdwLayoutCookie* \[ out\]
</dt> <dd>

Puntatore al buffer in cui questo metodo recupera un cookie di layout di tastiera soft.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                        | Descrizione                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Il metodo è stato eseguito correttamente.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o più parametri non sono validi.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile**](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)
</dt> <dt>

[**ISoftKbd::ShowSoftKeyboard**](isoftkbd-showsoftkeyboard.md)
</dt> </dl>

 

 





