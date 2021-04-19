---
description: La funzione AttachPropertyInstanceEx esegue il mapping di una proprietà esistente a una posizione specifica nei dati riconosciuti e modifica il valore dei dati della proprietà.
ms.assetid: 08bd1959-5ce8-4cb8-af8b-abbf4839c484
title: Funzione AttachPropertyInstanceEx (Netmon. h)
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
ms.openlocfilehash: 1e0841c49e54d10d38a56d6206bc255b0aa7c49a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311643"
---
# <a name="attachpropertyinstanceex-function"></a>AttachPropertyInstanceEx (funzione)

La funzione **AttachPropertyInstanceEx** esegue il mapping di una proprietà esistente a una posizione specifica nei dati riconosciuti e modifica il valore dei dati della proprietà.

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

*LengthEx* \[ in\]
</dt> <dd>

Lunghezza in byte dei dati estesi.

</dd> <dt>

*lpDataEx* \[ in\]
</dt> <dd>

Puntatore ai dati estesi, che è in genere una variabile dello stack che contiene i dati di estensione.

</dd> <dt>

*HelpID* \[ in\]
</dt> <dd>

Identificatore (compreso tra 0 e 2047) usato per impostare la Guida sensibile al contesto per una proprietà.

Il numero *HelpID* è relativo al file della Guida associato al database delle [*Proprietà*](p.md)del protocollo.

</dd> <dt>

*IndentLevel* \[ in\]
</dt> <dd>

Livello di rientro (compreso tra 0 e 15) utilizzato per visualizzare una proprietà gerarchicamente.

Network Monitor utilizza i livelli da 0 a 9. Il livello 15 è un valore speciale che consente al parser di alleghi una proprietà nascosta che non è visibile.

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

La funzione **AttachPropertyInstanceEx** viene chiamata durante l'implementazione della funzione di esportazione [**AttachProperties**](attachproperties.md) . Quando una proprietà viene associata ai dati tramite AttachPropertyInstanceEx, Network Monitor crea una struttura [**PROPERTYINST**](propertyinst.md) che definisce l'istanza della proprietà associata e una struttura [**PROPERTYINSTEX**](propertyinstex.md) che definisce i dati estesi.

Se viene chiamato **AttachPropertyInstanceEx** e non vengono forniti dati estesi, il parametro *lpDataEx* è **null** o il parametro *LengthEx* è 0, la chiamata **AttachPropertyInstanceEx** è equivalente dal punto di vista funzionale a una chiamata [**AttachPropertyInstance**](attachpropertyinstance.md) .

Durante l'implementazione di [**AttachProperties**](attachproperties.md), chiamare [**AttachPropertyInstance**](attachpropertyinstance.md) per usare i dati esistenti nell'acquisizione. È anche possibile chiamare la funzione **AttachPropertyInstanceEx** per modificare i dati della proprietà. Tuttavia, si consiglia di usare i dati esistenti nell'acquisizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




