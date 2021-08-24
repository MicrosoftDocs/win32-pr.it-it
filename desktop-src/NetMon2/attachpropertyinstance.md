---
description: La funzione AttachPropertyInstance esegue il mapping di una proprietà esistente a una posizione specifica nei dati riconosciuti.
ms.assetid: b44cf8d1-939b-45da-8a9a-b4bdcf9faf43
title: Funzione AttachPropertyInstance (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: c4d726b7500fd890dfe8c7fdc39f628c185dbe35f3a3bc14f0c05ab7f85cd673
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744681"
---
# <a name="attachpropertyinstance-function"></a>Funzione AttachPropertyInstance

La **funzione AttachPropertyInstance** esegue il mapping di una proprietà esistente a una posizione specifica nei dati riconosciuti.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI AttachPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ Pollici\]
</dt> <dd>

Handle per il frame che viene analizzato. Usare l'handle passato alla DLL del parser nel *parametro hFrame* della [**funzione AttachProperties.**](attachproperties.md)

</dd> <dt>

*hProperty* \[ Pollici\]
</dt> <dd>

Handle per una [**struttura PROPERTYINFO**](propertyinfo.md) che definisce la proprietà. Quando si implementa la [**funzione register**](register-parser.md) export, si specifica la **struttura PROPERTYINFO** che definisce la proprietà.

</dd> <dt>

*Lunghezza* \[ Pollici\]
</dt> <dd>

Lunghezza dei dati per questa istanza della proprietà .

</dd> <dt>

*lpData* \[ Pollici\]
</dt> <dd>

Puntatore alla posizione nei dati riconosciuti in cui si trova il valore della proprietà. Usare il puntatore passato alla DLL del parser *nel parametro lpProtocol* della [**funzione AttachProperties.**](attachproperties.md)

</dd> <dt>

*HELPID* \[ Pollici\]
</dt> <dd>

Identificatore (da 0 a 2047) usato per impostare la Guida sensibile al contesto per la proprietà .

Il numero di identificatore è relativo al file della Guida associato al database delle [*proprietà del protocollo*](p.md).

</dd> <dt>

*IndentLevel* \[ Pollici\]
</dt> <dd>

Livello di rientro (da 0 a 15) usato per visualizzare una proprietà in modo gerarchico.

Network Monitor usa i livelli da 0 a 14 per impostare un rientro per le proprietà. Il livello 15 è un valore speciale che consente a un parser di associare una proprietà nascosta non visibile.

</dd> <dt>

*Flag IFlags* \[ Pollici\]
</dt> <dd>

Valore del campo BIT che indica l'ordine dei BIT all'interno di una proprietà. I parser precedenti che *impostano fError* su 0 o 1 ora devono impostare *fError* su IFLAG \_ ERROR. Impostare questo parametro su uno dei valori seguenti.



| Valore                                                                                                                                                         | Significato                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <dt>**ERRORE \_ IFLAG**</dt> </dl>       | I dati nel frame hanno un errore.<br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <dt>**IFLAG \_ SWAPPED**</dt> </dl> | Al momento del collegamento, il byte **WORD** è un formato non Intel.<br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <dt>**IFLAG \_ UNICODE**</dt> </dl> | In fase di **collegamento, STRING** è Unicode.<br/>               |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **TRUE.**

Se la funzione ha esito negativo, il valore restituito è **FALSE.**

## <a name="remarks"></a>Commenti

La **funzione AttachPropertyInstance** viene chiamata durante l'implementazione della funzione di esportazione [**AttachProperties.**](attachproperties.md) Quando una proprietà è associata ai dati, Network Monitor crea una [**struttura PROPERTYINST**](propertyinst.md) che definisce l'istanza della proprietà associata.

Durante l'implementazione [**di AttachProperties,**](attachproperties.md)chiamare **AttachPropertyInstance** per usare i dati esistenti nell'acquisizione. È anche possibile chiamare [**la funzione AttachPropertyInstanceEx**](attachpropertyinstanceex.md) per modificare i dati della proprietà. Tuttavia, è consigliabile usare i dati così come sono presenti nell'acquisizione.



| Per informazioni su                                        | Vedere                                                                |
|-----------------------------------------------------------|--------------------------------------------------------------------|
| Che cosa sono i parser e come funzionano con Network Monitor. | [**Parser**](parsers.md)                                         |
| Come chiamare **AttachPropertyInstance**.                   | [Implementazione di AttachProperties](implementing-attachproperties.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietàallegato**](attachproperties.md)
</dt> <dt>

[**AttachPropertyInstanceEx**](attachpropertyinstanceex.md)
</dt> <dt>

[**PROPERTYINST**](propertyinst.md)
</dt> </dl>

 

 




