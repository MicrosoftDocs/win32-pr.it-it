---
description: Libera un blocco di memoria allocato da un heap da RtlAllocateHeap.
ms.assetid: 0A08FB6B-23A3-450B-8745-AEB927CEB7BB
title: Funzione RtlFreeHeap (Ntifs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlFreeHeap
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3dd46808c898cd934bbb4ee8804027bcb926e4a5cd07eb1521e2814a2c4b0e1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538075"
---
# <a name="rtlfreeheap-function"></a>Funzione RtlFreeHeap

Libera un blocco di memoria allocato da un heap da [**RtlAllocateHeap.**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)

## <a name="syntax"></a>Sintassi


```C++
BOOLEAN RtlFreeHeap(
  _In_     PVOID HeapHandle,
  _In_opt_ ULONG Flags,
  _In_     PVOID HeapBase
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HeapHandle* \[ Pollici\]
</dt> <dd>

Handle per l'heap il cui blocco di memoria deve essere liberato. Questo parametro è un handle restituito [**da RtlCreateHeap.**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)

</dd> <dt>

*Flag* \[ in, facoltativo\]
</dt> <dd>

Set di flag che controlla gli aspetti della liberazione di un blocco di memoria. Se si specifica il valore seguente, viene eseguito l'override del valore corrispondente specificato nel parametro *Flags* quando l'heap è stato creato da [**RtlCreateHeap.**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)



| Contrassegno                           | Significato                                                                                   |
|--------------------------------|-------------------------------------------------------------------------------------------|
| HEAP \_ SENZA \_ SERIALIZZAZIONE<br/> | L'esclusione reciproca non verrà usata **quando RtlFreeHeap** accede all'heap. <br/> |



 

</dd> <dt>

*HeapBase* \[ Pollici\]
</dt> <dd>

Puntatore al blocco di memoria da liberare. Questo puntatore viene restituito [**da RtlAllocateHeap.**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** il blocco è stato liberato correttamente. **FALSE in** caso contrario.

> [!Note]  
> A partire Windows 8 il valore restituito viene tipiato come **LOGICAL,** che ha una dimensione diversa rispetto a **BOOLEAN.**

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                    |
| Piattaforma di destinazione<br/>          | <dl> <dt>[Universale](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Intestazione<br/>                   | <dl> <dt>Ntifs.h (includere Ntifs.h)</dt> </dl>                                    |
| Libreria<br/>                  | <dl> <dt>Ntdll.lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)
</dt> <dt>

[**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)
</dt> <dt>

[**RtlDestroyHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtldestroyheap)
</dt> </dl>

 

 
