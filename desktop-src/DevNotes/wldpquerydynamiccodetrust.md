---
description: Recupera un valore che determina se il codice dinamico del CRL .NET in memoria o su disco è considerato attendibile dai criteri di Device Guard.
ms.assetid: 9C12894D-98AF-4408-A11A-865E4DA1DA68
title: Funzione WldpQueryDynamicCodeTrust (Wldp. h)
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
ms.openlocfilehash: 1b9b3cc30f5a02ae86fd8a30043a9ab417ec1ac7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523466"
---
# <a name="wldpquerydynamiccodetrust-function"></a>WldpQueryDynamicCodeTrust (funzione)

Recupera un valore che determina se il codice dinamico del CRL .NET in memoria o su disco è considerato attendibile dai criteri di Device Guard.

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

*fileHandle* 
</dt> <dd>

Handle per il file di codice dinamico su disco da verificare. Se *filehandle* è diverso da **null**, *baseImage* deve essere **null**.

</dd> <dt>

*baseImage* 
</dt> <dd>

Puntatore al file PE in memoria da controllare. Se *baseImage* è diverso da **null**, *filehandle* deve essere **null**.

</dd> <dt>

*ImageSize* 
</dt> <dd>

Quando *baseImage* è diverso da **null**, indica le dimensioni del buffer a cui punta *baseImage* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce **\_ OK** se l'esito è positivo o un codice di errore; in caso contrario,.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




