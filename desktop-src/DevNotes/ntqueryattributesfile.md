---
description: Recupera gli attributi di base per l'oggetto file specificato.
ms.assetid: 19f9a2ac-4db6-4c67-9f85-c107063e11b8
title: NtQueryAttributesFile (funzione)
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
ms.openlocfilehash: a1d6d2ff20539f5ef65c0886ba51a0dbabafb44d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326093"
---
# <a name="ntqueryattributesfile-function"></a>NtQueryAttributesFile (funzione)

\[Questa funzione può essere modificata o rimossa da Windows senza ulteriore preavviso.\]

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

*ObjectAttributes* \[ in\]
</dt> <dd>

Puntatore a una struttura [degli \_ attributi dell'oggetto](https://msdn.microsoft.com/library/aa491657.aspx) che fornisce gli attributi da utilizzare per l'oggetto file.

</dd> <dt>

*Informazioni FileInformation* \[ out\]
</dt> <dd>

Puntatore a una struttura [di \_ \_ informazioni di base del file](https://msdn.microsoft.com/library/aa491634.aspx) per ricevere le informazioni sugli attributi del file restituito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un codice NTSTATUS o Error.

I moduli e il significato dei codici di errore NTSTATUS sono elencati nel file di intestazione Ntstatus. h disponibile in WDK e sono descritti nella documentazione di WDK.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione. La libreria di importazione associata, Ntdll. lib, è disponibile in WDK. È anche possibile usare le funzioni [**LoadLibrary**](-loadlibrary.md) e [**GetProcAddress**](-getprocaddress-.md) per eseguire un collegamento dinamico a Ntdll.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 




