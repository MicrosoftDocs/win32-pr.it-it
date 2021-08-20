---
title: Metodo IVMKeyboard TypeKeySequence (VPCCOMInterfaces.h)
description: Simula un elenco delimitato da virgole di chiavi digitate.
ms.assetid: ba4d4e43-cb2e-49ae-940d-2e81286d3473
keywords:
- Metodo TypeKeySequence Virtual PC
- Metodo TypeKeySequence Virtual PC, interfaccia IVMKeyboard
- Interfaccia IVMKeyboard Virtual PC, metodo TypeKeySequence
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeKeySequence
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565d31d04a31f72ea25b3477fb91d53d252f6173eec8bc2f40133db38eeb1619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998861"
---
# <a name="ivmkeyboardtypekeysequence-method"></a>Metodo IVMKeyboard::TypeKeySequence

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Simula un elenco delimitato da virgole di chiavi digitate.

## <a name="syntax"></a>Sintassi


```C++
HRESULT TypeKeySequence(
  [in] BSTR keySequence
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*keySequence* \[ Pollici\]
</dt> <dd>

Sequenza delimitata da virgole di codici chiave da digitare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                 | Descrizione                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>                                   |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **NULL.**<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | La stringa specificata è vuota o contiene un codice di chiave non valido.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Si è verificato un errore imprevisto.<br/>                               |



 

## <a name="remarks"></a>Commenti

Una stringa di sequenza di tasti è un set delimitato da virgole di identificatori di tasto usati per simulare la sequenza di pressione e rilascio di una tastiera AT standard di tipo U.S. 101.

Se nella stringa viene visualizzato un identificatore di tasto senza un modificatore precedente, alla sessione della macchina virtuale viene inviato un codice premuto dal tasto, seguito immediatamente dal codice rilasciato dal tasto corrispondente. I modificatori di tasti possono essere usati per modificare questo comportamento.

Ad esempio, il modificatore DOWN invierà il codice premuto dal tasto per l'identificatore di tasto seguente senza inviare il codice rilasciato dal tasto. Ciò è utile per simulare i tasti CTRL, ALT e MAIUSC quando vengono mantenuti mentre vengono inviati altri tasti. Per rilasciare la chiave, è necessario includerla nuovamente nella stringa chiave insieme a un modificatore UP precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMKeyboard è definito come \_ 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> <dt>

[Sequenze di tasti](key-sequences.md)
</dt> </dl>

 

