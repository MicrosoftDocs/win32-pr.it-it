---
title: Funzione UtilAssembleStringsWithAlloc (Ndattributils.h)
description: Alloca una stringa e la formatta usando le stringhe fornite dalla tabella delle stringhe. Questa funzione usa StringCchPrintf per creare la stringa formattata.
ms.assetid: eedc2874-b949-4cc2-ba7c-ebf1924f1156
keywords:
- Funzione UtilAssembleStringsWithAlloc NDF
topic_type:
- apiref
api_name:
- UtilAssembleStringsWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38473f45e2bd4c53b964bb38ec285cdf3eea091a96d72684c1d801b949f4d0a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801731"
---
# <a name="utilassemblestringswithalloc-function"></a>Funzione UtilAssembleStringsWithAlloc

La **funzione UtilAssembleStringsWithAlloc** alloca una stringa e la formatta usando le stringhe fornite dalla tabella delle stringhe. Questa funzione usa [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) per creare la stringa formattata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UtilAssembleStringsWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR InputFormat,
  _In_  LPCWSTR InputString,
  _In_  BOOLEAN AdditionalArgument,
  _In_  ULONG   AdditionalValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Buffer* \[ Cambio\]
</dt> <dd>

Tipo: **LPWSTR \***

Posizione in cui verrà inserita la stringa appena allocata. Quando la stringa non è più necessaria, deve essere rilasciata con [**CoTaskMemFree.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)

</dd> <dt>

*BufferMax* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Numero massimo di caratteri consentiti nella stringa allocata da *Buffer*. Se la stringa formattata risultante è più lunga del numero di caratteri specificato, viene troncata e con terminazione Null.

> [!Note]  
> Questo parametro non può essere impostato su zero.

 

</dd> <dt>

*InputFormat* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR**

Risorsa stringa dalla tabella di stringhe che rappresenta un parametro di formato passato a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa). Viene costruito usando [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).

Il formato della stringa di risorsa deve specificare un parametro di formato che prende una stringa wide o un parametro di formato che prende un valore long senza segno e una stringa wide.

</dd> <dt>

*InputString* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR**

Risorsa stringa dalla tabella di stringhe che rappresenta un argomento passato a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) al posto della stringa wide nel parametro format. Viene costruito usando [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).

</dd> <dt>

*AdditionalArgument* \[ Pollici\]
</dt> <dd>

Tipo: **BOOLEAN**

True se *AdditionalValue* deve essere passato come primo argomento di formattazione [**a StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa); in caso contrario, false (e verrà passata solo la stringa di risorsa identificata da *InputString).*

</dd> <dt>

*AdditionalValue* \[ Pollici\]
</dt> <dd>

Tipo: **ULONG**

Valore da passare come primo argomento di formattazione a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) se *AdditionalArgument* è true.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

I possibili valori restituiti includono, ma non solo, quanto segue.



| Codice restituito                                                                                  | Descrizione                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione completata.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o più parametri non sono stati forniti correttamente.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Ndattributils.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**UtilStringCopyWithAlloc**](utilstringcopywithalloc.md)
</dt> <dt>

[**UtilLoadStringWithAlloc**](utilloadstringwithalloc.md)
</dt> <dt>

[**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)
</dt> <dt>

[**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

