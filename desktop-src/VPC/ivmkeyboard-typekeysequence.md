---
title: Metodo IVMKeyboard TypeKeySequence (VPCCOMInterfaces. h)
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
ms.openlocfilehash: c34bd96077c1d28aad196ee0d6b11de122725d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964874"
---
# <a name="ivmkeyboardtypekeysequence-method"></a>Metodo IVMKeyboard:: TypeKeySequence

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Simula un elenco delimitato da virgole di chiavi digitate.

## <a name="syntax"></a>Sintassi


```C++
HRESULT TypeKeySequence(
  [in] BSTR keySequence
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sequenza di sequenze* \[ in\]
</dt> <dd>

Sequenza delimitata da virgole dei codici chiave da tipizzare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                 | Descrizione                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>                                   |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **null**.<br/>                                      |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>      | La stringa specificata è vuota o contiene un codice chiave non valido.<br/> |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl> | Si è verificato un errore imprevisto.<br/>                               |



 

## <a name="remarks"></a>Commenti

Una stringa di sequenza di chiavi è un set delimitato da virgole di identificatori di chiave usati per simulare la sequenza di stampa e di rilascio della chiave di una tastiera standard in stile US 101-Key.

Se un identificatore di chiave viene visualizzato nella stringa senza un modificatore precedente, viene inviato un codice con pressione di tasto alla sessione della macchina virtuale, seguito immediatamente dal codice corrispondente rilasciato dalla chiave. Per modificare questo comportamento, è possibile usare i modificatori di chiave.

Il modificatore DOWN, ad esempio, invierà il codice premuto per la chiave per l'identificatore di chiave seguente senza inviare il codice rilasciato dalla chiave. Questa operazione è utile per la simulazione dei tasti CTRL, ALT e MAIUSC quando vengono mantenuti mentre sono in corso l'invio di altri tasti. Per rilasciare la chiave, è necessario includerla nuovamente nella stringa della chiave insieme a un modificatore UP precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard è definito come 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> <dt>

[Sequenze di chiavi](key-sequences.md)
</dt> </dl>

 

