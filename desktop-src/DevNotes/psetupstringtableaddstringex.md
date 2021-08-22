---
description: Aggiunge una stringa e dati aggiuntivi a una tabella.
ms.assetid: e6f29cb0-4468-435d-9ae3-217d4f69e87e
title: Funzione pSetupStringTableAddStringEx
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
ms.openlocfilehash: 69aef5b206bec609aefd66b33bfa838471b944292767642aeef28f734c9c47b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386421"
---
# <a name="psetupstringtableaddstringex-function"></a>Funzione pSetupStringTableAddStringEx

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

*StringTable* \[ Pollici\]
</dt> <dd>

Puntatore alla tabella di stringhe.

</dd> <dt>

*Stringa* \[ Pollici\]
</dt> <dd>

Puntatore alla stringa da aggiungere alla tabella.

</dd> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Il valore di questo parametro può essere `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA` .



| Valore                                                                                                                                                                                                                                             | Significato                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="STRTAB_CASE_SENSITIVE"></span><span id="strtab_case_sensitive"></span><dl> <dt>**STRTAB \_ \_Maiuscole/minuscole**</dt> <dt>0x001</dt> </dl> | La stringa fa distinzione tra maiuscole e minuscole.<br/> |
| <span id="STRTAB_NEW_EXTRADATA"></span><span id="strtab_new_extradata"></span><dl> <dt>**STRTAB \_ NUOVO \_ 0x004 EXTRADATA**</dt> <dt></dt> </dl>    | Sono disponibili dati aggiuntivi.<br/>      |



 

</dd> <dt>

*ExtraData* \[ in, facoltativo\]
</dt> <dd>

Puntatore facoltativo a un oggetto dati aggiuntivo.

</dd> <dt>

*ExtraDataSize* \[ in, facoltativo\]
</dt> <dd>

Dimensioni dei dati aggiuntivi.

</dd> </dl>

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
