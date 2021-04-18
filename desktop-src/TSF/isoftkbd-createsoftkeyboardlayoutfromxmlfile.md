---
title: Metodo ISoftKbd CreateSoftKeyboardLayoutFromXMLFile (Softkbdc. h)
description: Il metodo ISoftKbd CreateSoftKeyboardLayoutFromXMLFile crea un layout di tastiera soft dal file XML specificato.
ms.assetid: e665adab-1d75-4e41-87bf-c8ce0f7a0399
keywords:
- Framework servizi di testo Metodo CreateSoftKeyboardLayoutFromXMLFile
- Framework dei servizi di testo del metodo CreateSoftKeyboardLayoutFromXMLFile, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo CreateSoftKeyboardLayoutFromXMLFile
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromXMLFile
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252db845c5e1cc732adc295e1989fee83d4ac6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302102"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromxmlfile-method"></a>Metodo ISoftKbd:: CreateSoftKeyboardLayoutFromXMLFile

Il metodo **ISoftKbd:: CreateSoftKeyboardLayoutFromXMLFile** crea un layout di tastiera soft dal file XML specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateSoftKeyboardLayoutFromXMLFile(
  [in]  WCHAR *lpszKeyboardDesFile,
  [in]  INT   szFileStrLen,
  [out] DWORD *pdwLayoutCookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszKeyboardDesFile* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione zero che indica il nome del file XML.

</dd> <dt>

*szFileStrLen* \[ in\]
</dt> <dd>

Stringa con terminazione zero che indica la lunghezza del file XML.

</dd> <dt>

*pdwLayoutCookie* \[ out\]
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

[**ISoftKbd::CreateSoftKeyboardLayoutFromResource**](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> </dl>

 

 





