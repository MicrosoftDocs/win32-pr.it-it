---
description: Recupera un valore che determina se il codice dinamico CRL .NET in memoria o su disco specificato è considerato attendibile dai criteri di Device Guard.
ms.assetid: 9C12894D-98AF-4408-A11A-865E4DA1DA68
title: Funzione WldpQueryDynamicCodeTrust (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 00b26c8d237a8c6d725751be064c7b82fc7a600c452598a590a747ba10ae56d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075725"
---
# <a name="wldpquerydynamiccodetrust-function"></a>Funzione WldpQueryDynamicCodeTrust

Recupera un valore che determina se il codice dinamico CRL .NET in memoria o su disco specificato è considerato attendibile dai criteri di Device Guard.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI WldpQueryDynamicCodeTrust(
   _When_(baseImage != NULL, _In_opt_)
    _When_(baseImage == NULL, _In_)
    HANDLE                                                 fileHandle,
   _When_(fileHandle == NULL, _In_reads_bytes_opt_(imageSize))
    _When_(fileHandle != NULL, _In_reads_bytes_(imageSize))
    PVOID  baseImage,
   _In_ ULONG                                                                                                                         ImageSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Filehandle* 
</dt> <dd>

Handle al file di codice dinamico su disco da controllare. Se *fileHandle* non è **NULL,** *baseImage* deve essere **NULL.**

</dd> <dt>

*baseImage* 
</dt> <dd>

Puntatore al file PE in memoria da controllare. Se *baseImage* non è **NULL,** *FileHandle* deve essere **NULL.**

</dd> <dt>

*Imagesize* 
</dt> <dd>

Quando *baseImage* è diverso da **NULL,** indica le dimensioni del buffer a cui *punta baseImage.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce **S \_ OK in caso** di esito positivo o un codice di errore in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wldp.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




