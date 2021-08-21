---
description: La funzione Extract estrae i file da un file CAB.
ms.assetid: c6a79d81-7adf-4b8e-a1ef-fec868f7fdbf
title: Estrarre la funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extract
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: cbcb53aae008423ac56bb489d43f6fd78016a9b1f716be21390a6dfc1de00404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162065"
---
# <a name="extract-function"></a>Estrarre la funzione

\[Questa funzione non è più supportata, pertanto il relativo comportamento non può essere garantito.\]

La **funzione Extract** estrae i file da un file CAB.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Extract(
   PSESSION ps,
   LPCSTR   lpCabName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Ps* 
</dt> <dd>

Puntatore a una struttura [**SESSION**](session.md) che contiene informazioni sulla sessione corrente.

</dd> <dt>

*lpCabName* 
</dt> <dd>

Puntatore al nome del file CAB da cui estrarre i file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **S \_ OK;** in caso contrario, restituisce un codice di errore.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DeleteExtractedFiles**](deleteextractedfiles.md)
</dt> <dt>

[**Erf**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf)
</dt> <dt>

[**Sessione**](session.md)
</dt> </dl>

 

 
