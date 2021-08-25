---
description: La funzione AttachPropertyInstanceEx esegue il mapping di una proprietà esistente a una posizione specifica nei dati riconosciuti e modifica il valore dei dati della proprietà.
ms.assetid: 08bd1959-5ce8-4cb8-af8b-abbf4839c484
title: Funzione AttachPropertyInstanceEx (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstanceEx
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e184ec0b874d55d149c9d049b8c6b2cafd716fe82c66410e2d3e1550b397c366
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911281"
---
# <a name="attachpropertyinstanceex-function"></a>Funzione AttachPropertyInstanceEx

La **funzione AttachPropertyInstanceEx** esegue il mapping di una proprietà esistente a una posizione specifica nei dati riconosciuti e modifica il valore dei dati della proprietà.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI AttachPropertyInstanceEx(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     LengthEx,
  _In_ ULPVOID   lpDataEx,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ Pollici\]
</dt> <dd>

Handle per il frame in fase di analisi. Usare l'handle passato alla DLL del parser nel *parametro hFrame* della [**funzione AttachProperties.**](attachproperties.md)

</dd> <dt>

*hProperty* \[ Pollici\]
</dt> <dd>

Handle a una [**struttura PROPERTYINFO**](propertyinfo.md) che definisce la proprietà. Quando si implementa la [**funzione Register**](register-parser.md) export si specifica la **struttura PROPERTYINFO** che definisce la proprietà.

</dd> <dt>

*Lunghezza* \[ Pollici\]
</dt> <dd>

Lunghezza dei dati per questa istanza della proprietà .

</dd> <dt>

*lpData* \[ Pollici\]
</dt> <dd>

Puntatore alla posizione nei dati riconosciuti in cui si trova il valore della proprietà. Usare il puntatore passato alla DLL del parser *nel parametro lpProtocol* della [**funzione AttachProperties.**](attachproperties.md)

</dd> <dt>

*LengthEx* \[ Pollici\]
</dt> <dd>

Lunghezza in byte della lunghezza dei dati estesa.

</dd> <dt>

*lpDataEx* \[ Pollici\]
</dt> <dd>

Puntatore ai dati estesi, che in genere è una variabile dello stack che contiene i dati di estensione.

</dd> <dt>

*HelpID* \[ Pollici\]
</dt> <dd>

Identificatore (da 0 a 2047) utilizzato per impostare la Guida sensibile al contesto per una proprietà.

Il *numero HelpID* è relativo al file della Guida associato al database delle [*proprietà del protocollo*](p.md).

</dd> <dt>

*IndentLevel* \[ Pollici\]
</dt> <dd>

Livello di rientro (da 0 a 15) usato per visualizzare una proprietà in modo gerarchico.

Network Monitor usa i livelli da 0 a 9. Il livello 15 è un valore speciale che consente al parser di associare una proprietà nascosta non visibile.

</dd> <dt>

*IFlags* \[ Pollici\]
</dt> <dd>

Valore del campo BIT che indica l'ordine dei BIT all'interno di una proprietà. I parser precedenti che impostano *fError* su 0 o 1 dovrebbero ora impostare *fError* su IFLAG \_ ERROR. Impostare questo parametro su uno dei valori seguenti.



| Valore                                                                                                                                                         | Significato                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <dt>**ERRORE \_ IFLAG**</dt> </dl>       | I dati nel frame hanno un errore.<br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <dt>**IFLAG \_ SCAMBIATO**</dt> </dl> | Al momento del collegamento, il byte **WORD** è un formato non Intel.<br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <dt>**IFLAG \_ UNICODE**</dt> </dl> | In fase di **collegamento, STRING** è Unicode.<br/>               |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **TRUE.**

Se la funzione ha esito negativo, il valore restituito è **FALSE.**

## <a name="remarks"></a>Commenti

La **funzione AttachPropertyInstanceEx** viene chiamata durante l'implementazione della funzione di esportazione [**AttachProperties.**](attachproperties.md) Quando una proprietà viene associata ai dati usando AttachPropertyInstanceEx, Network Monitor crea una struttura [**PROPERTYINST**](propertyinst.md) che definisce l'istanza della proprietà associata e una struttura [**PROPERTYINSTEX**](propertyinstex.md) che definisce i dati estesi.

Se **viene chiamato AttachPropertyInstanceEx** e non vengono forniti dati estesi, il parametro *lpDataEx* è **NULL** o il parametro *LengthEx* è 0, la chiamata **a AttachPropertyInstanceEx** è funzionalmente equivalente a una chiamata a [**AttachPropertyInstance.**](attachpropertyinstance.md)

Durante l'implementazione [**di AttachProperties,**](attachproperties.md) [**chiamare AttachPropertyInstance**](attachpropertyinstance.md) per usare i dati così come sono presenti nell'acquisizione. È anche possibile chiamare **la funzione AttachPropertyInstanceEx** per modificare i dati della proprietà. Tuttavia, è consigliabile usare i dati così come sono presenti nell'acquisizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




