---
description: Aggiunge una stringa e dati aggiuntivi a una tabella.
ms.assetid: e6f29cb0-4468-435d-9ae3-217d4f69e87e
title: pSetupStringTableAddStringEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableAddStringEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 22de3bcc2ad21b82e1fd8306a0c668f83c723b9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326440"
---
# <a name="psetupstringtableaddstringex-function"></a>pSetupStringTableAddStringEx (funzione)

\[Questa funzione non è disponibile in Windows Vista o Windows Server 2008.\]

Aggiunge una stringa e dati aggiuntivi a una tabella.

## <a name="syntax"></a>Sintassi


```C++
LONG pSetupStringTableAddStringEx(
  _In_     PVOID StringTable,
  _In_     PTSTR String,
  _In_     DWORD Flags,
  _In_opt_ PVOID ExtraData,
  _In_opt_ UINT  ExtraDataSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Un'STRINGTABLE* \[ in\]
</dt> <dd>

Puntatore alla tabella delle stringhe.

</dd> <dt>

*Stringa* \[ di in\]
</dt> <dd>

Puntatore alla stringa da aggiungere alla tabella.

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Il valore di questo parametro può essere `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA` .



| Valore                                                                                                                                                                                                                                             | Significato                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="STRTAB_CASE_SENSITIVE"></span><span id="strtab_case_sensitive"></span><dl> <dt>**STRTAB \_ 0x001 \_ maiuscole/minuscole**</dt> <dt></dt> </dl> | La stringa fa distinzione tra maiuscole e minuscole.<br/> |
| <span id="STRTAB_NEW_EXTRADATA"></span><span id="strtab_new_extradata"></span><dl> <dt>**STRTAB \_ NUOVO \_**</dt> <dt>0x004</dt> di dati </dl>    | Sono presenti dati aggiuntivi.<br/>      |



 

</dd> <dt>

*Dati* \[ di in, facoltativo\]
</dt> <dd>

Puntatore facoltativo a un oggetto dati aggiuntivo.

</dd> <dt>

*ExtraDataSize* \[ in, facoltativo\]
</dt> <dd>

Dimensione dei dati aggiuntivi.

</dd> </dl>

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
