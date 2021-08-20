---
description: Recupera gli attributi di base per l'oggetto file specificato.
ms.assetid: 19f9a2ac-4db6-4c67-9f85-c107063e11b8
title: Funzione NtQueryAttributesFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryAttributesFile
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: e6b1ecdc7cc7f0a5c18afc3eeb613c3f9cd9a38aa22a876ad156c3d1c6b1bc97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826807"
---
# <a name="ntqueryattributesfile-function"></a>Funzione NtQueryAttributesFile

\[Questa funzione può essere modificata o rimossa da Windows senza preavviso.\]

Recupera gli attributi di base per l'oggetto file specificato.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS NtQueryAttributesFile(
  _In_  POBJECT_ATTRIBUTES      ObjectAttributes,
  _Out_ PFILE_BASIC_INFORMATION FileInformation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ObjectAttributes* \[ Pollici\]
</dt> <dd>

Puntatore a una [struttura OBJECT \_ ATTRIBUTES](https://msdn.microsoft.com/library/aa491657.aspx) che fornisce gli attributi da utilizzare per l'oggetto file.

</dd> <dt>

*FileInformation* \[ Cambio\]
</dt> <dd>

Puntatore a una struttura [FILE \_ BASIC \_ INFORMATION](https://msdn.microsoft.com/library/aa491634.aspx) per ricevere le informazioni sull'attributo del file restituito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un CODICE NTSTATUS o di errore.

I moduli e il significato dei codici di errore NTSTATUS sono elencati nel file di intestazione Ntstatus.h disponibile in WDK e sono descritti nella documentazione di WDK.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione. La libreria di importazione associata, Ntdll.lib, è disponibile in WDK. È anche possibile usare le [**funzioni LoadLibrary**](-loadlibrary.md) e [**GetProcAddress**](-getprocaddress-.md) per collegarsi dinamicamente Ntdll.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 




