---
description: Completa la configurazione di un buffer di traccia con campi facoltativi per le tracce di tipo sprintf.
ms.assetid: a5f3ecbe-d335-4fd0-99aa-4d5a748ca4e1
title: AsyncStringTrace (funzione)
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
ms.openlocfilehash: 15bfff82f5ef0ae3f921a3a4c83b4d35fb83d95f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326682"
---
# <a name="asyncstringtrace-function"></a>AsyncStringTrace (funzione)

Completa la configurazione di un buffer di traccia con campi facoltativi per le tracce di tipo **sprintf**.

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

*marcatore* 
</dt> <dd>

Marcatore per le funzioni **vsprintf** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce la lunghezza, in byte, dell'istruzione Trace.

## <a name="remarks"></a>Commenti

Exstrace.dll è un componente facoltativo che viene installato con il Simple Mail Transfer Protocol (SMTP) e il protocollo NNTP (Network News Transfer Protocol).

Il tipo di dati **va \_ List** è un tipo standard usato per conservare le informazioni necessarie per le macro **va \_ arg** e **va \_ end** . Per ulteriori informazioni, vedere [tipi standard](/cpp/c-runtime-library/standard-types?view=vs-2019).

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

