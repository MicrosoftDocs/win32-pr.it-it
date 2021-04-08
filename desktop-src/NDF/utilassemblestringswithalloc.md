---
title: Funzione UtilAssembleStringsWithAlloc (Ndattributils. h)
description: Alloca una stringa e la formatta usando le stringhe fornite dalla tabella delle stringhe. Questa funzione USA StringCchPrintf per creare la stringa formattata.
ms.assetid: eedc2874-b949-4cc2-ba7c-ebf1924f1156
keywords:
- UtilAssembleStringsWithAlloc funzione NDF
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
ms.openlocfilehash: dae121b1d5f2d968f696190c64828be91adc71da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743882"
---
# <a name="utilassemblestringswithalloc-function"></a>UtilAssembleStringsWithAlloc (funzione)

La funzione **UtilAssembleStringsWithAlloc** alloca una stringa e la formatta usando le stringhe fornite dalla tabella delle stringhe. Questa funzione usa [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) per creare la stringa formattata.

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

*Buffer* \[ out\]
</dt> <dd>

Tipo: **LPWSTR \** _

Posizione in cui verrà posizionata la stringa appena allocata. Quando la stringa non è più necessaria, deve essere rilasciata con [_ *CoTaskMemFree* *](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*BufferMax* \[ in\]
</dt> <dd>

Tipo: **uint**

Numero massimo di caratteri consentiti nella stringa allocata dal *buffer*. Se la stringa formattata risultante supera il numero di caratteri specificato, viene troncata e terminata con null.

> [!Note]  
> Questo parametro non può essere impostato su zero.

 

</dd> <dt>

*InputFormat* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Risorsa di stringa fuori dalla tabella delle stringhe che rappresenta un parametro di formato passato a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa). Viene costruito usando [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).

Il formato della stringa di risorsa deve specificare un parametro di formato che accetta una stringa di caratteri "wide" oppure un parametro di formato che accetta un valore long senza segno e una stringa di caratteri "wide".

</dd> <dt>

*InputString* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Risorsa di tipo stringa fuori dalla tabella delle stringhe che rappresenta un argomento passato a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) al posto della stringa estesa nel parametro format. Viene costruito usando [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).

</dd> <dt>

*AdditionalArgument* \[ in\]
</dt> <dd>

Tipo: **booleano**

True se *AdditionalValue* deve essere passato come primo argomento di formattazione a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa); in caso contrario, false (verrà passata solo la stringa di risorsa identificata da *InputString* ).

</dd> <dt>

*AdditionalValue* \[ in\]
</dt> <dd>

Tipo: **ULONG**

Valore da passare come primo argomento di formattazione a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) se *AdditionalArgument* è true.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

I valori restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice restituito                                                                                  | Descrizione                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Operazione completata.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o più parametri non sono stati specificati correttamente.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                 |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



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

 

