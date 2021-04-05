---
description: La funzione AttachPropertyInstance esegue il mapping di una proprietà esistente a una posizione specifica nei dati riconosciuti.
ms.assetid: b44cf8d1-939b-45da-8a9a-b4bdcf9faf43
title: Funzione AttachPropertyInstance (Netmon. h)
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
ms.openlocfilehash: 50ab07967605f8a24ba330a3cb13f80c833cf542
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883674"
---
# <a name="attachpropertyinstance-function"></a>AttachPropertyInstance (funzione)

La funzione **AttachPropertyInstance** esegue il mapping di una proprietà esistente a una posizione specifica nei dati riconosciuti.

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

*hFrame* \[ in\]
</dt> <dd>

Handle per il frame da analizzare. Usare l'handle passato alla DLL del parser nel parametro *hFrame* della funzione [**AttachProperties**](attachproperties.md) .

</dd> <dt>

*hProperty* \[ in\]
</dt> <dd>

Handle per una struttura [**PROPERTYINFO**](propertyinfo.md) che definisce la proprietà. Quando si implementa la funzione di esportazione del [**Registro**](register-parser.md) , è necessario specificare la struttura **PROPERTYINFO** che definisce la proprietà.

</dd> <dt>

*Lunghezza* \[ in\]
</dt> <dd>

Lunghezza dei dati per questa istanza della proprietà.

</dd> <dt>

*lpData* \[ in\]
</dt> <dd>

Puntatore alla posizione nei dati riconosciuti in cui si trova il valore della proprietà. Usare il puntatore passato alla DLL del parser nel parametro *lpProtocol* della funzione [**AttachProperties**](attachproperties.md) .

</dd> <dt>

*HelpID* \[ in\]
</dt> <dd>

Identificatore (compreso tra 0 e 2047) usato per impostare la Guida sensibile al contesto per la proprietà.

Il numero dell'identificatore è relativo al file della Guida associato al [*database della proprietà*](p.md)del protocollo.

</dd> <dt>

*IndentLevel* \[ in\]
</dt> <dd>

Livello di rientro (compreso tra 0 e 15) utilizzato per visualizzare una proprietà gerarchicamente.

Network Monitor utilizza i livelli da 0 a 14 per rientrare le proprietà. Il livello 15 è un valore speciale che consente a un parser di alleghi una proprietà nascosta che non è visibile.

</dd> <dt>

*IFlags* \[ in\]
</dt> <dd>

Valore del campo di BIT che indica l'ordine dei bit all'interno di una proprietà. I parser precedenti che impostano il *ferror* su 0 o 1 devono ora impostare il *ferror* su IFLAG \_ Error. Impostare questo parametro su uno dei valori seguenti.



| Valore                                                                                                                                                         | Significato                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <dt>**\_errore IFLAG**</dt> </dl>       | Si è verificato un errore nei dati del frame.<br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <dt>**IFLAG \_ scambiati**</dt> </dl> | Al momento della connessione, **Word** byte è un formato non Intel.<br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <dt>**IFLAG \_ Unicode**</dt> </dl> | Al momento della connessione, la **stringa** è Unicode.<br/>               |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **true**.

Se la funzione ha esito negativo, il valore restituito è **false**.

## <a name="remarks"></a>Commenti

La funzione **AttachPropertyInstance** viene chiamata durante l'implementazione della funzione di esportazione [**AttachProperties**](attachproperties.md) . Quando una proprietà è associata ai dati, Network Monitor crea una struttura [**PROPERTYINST**](propertyinst.md) che definisce l'istanza della proprietà associata.

Durante l'implementazione di [**AttachProperties**](attachproperties.md), chiamare **AttachPropertyInstance** per usare i dati esistenti nell'acquisizione. È anche possibile chiamare la funzione [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) per modificare i dati della proprietà. Tuttavia, si consiglia di usare i dati esistenti nell'acquisizione.



| Per informazioni su                                        | Vedere                                                                |
|-----------------------------------------------------------|--------------------------------------------------------------------|
| Quali sono i parser e come funzionano con Network Monitor. | [**Parser**](parsers.md)                                         |
| Come chiamare **AttachPropertyInstance**.                   | [Implementazione di AttachProperties](implementing-attachproperties.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AttachProperties**](attachproperties.md)
</dt> <dt>

[**AttachPropertyInstanceEx**](attachpropertyinstanceex.md)
</dt> <dt>

[**PROPERTYINST**](propertyinst.md)
</dt> </dl>

 

 




