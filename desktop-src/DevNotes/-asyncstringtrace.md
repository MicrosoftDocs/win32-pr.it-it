---
description: 'Funzione AsyncStringTrace: completa la configurazione di un buffer di traccia con campi facoltativi per le tracce in stile sprintf.'
ms.assetid: a5f3ecbe-d335-4fd0-99aa-4d5a748ca4e1
title: Funzione AsyncStringTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncStringTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: 342670dc406cb84588984d0a9ab10fae280c5483
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085799"
---
# <a name="asyncstringtrace-function"></a>Funzione AsyncStringTrace

Completa la configurazione di un buffer di traccia con campi facoltativi per le tracce in stile **sprintf.**

## <a name="syntax"></a>Sintassi


```C++
int AsyncStringTrace(
   LPARAM  lParam,
   LPCSTR  szFormat,
   va_list marker
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Parametro di traccia a 32 bit utilizzato per il filtro a livello di applicazione.

</dd> <dt>

*szFormat* 
</dt> <dd>

Stringa con terminazione zero che descrive il formato della traccia.

</dd> <dt>

*Marcatore* 
</dt> <dd>

Marcatore per **le funzioni vsprintf.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce la lunghezza dell'istruzione di traccia, in byte.

## <a name="remarks"></a>Commenti

Exstrace.dll è un componente facoltativo che viene installato con il Simple Mail Transfer Protocol (SMTP) e il protocollo NNTP (Network News Transfer Protocol).

Il **tipo di dati va \_ list** è un tipo standard usato per contenere le informazioni necessarie per le macro **va \_ arg** e **va \_ end.** Per altre informazioni, vedere [Tipi standard.](/cpp/c-runtime-library/standard-types?view=vs-2019)

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

