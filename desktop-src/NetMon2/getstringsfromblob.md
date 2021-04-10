---
description: USA chiamate sequenziali per recuperare tutte le stringhe all'interno di intervalli specificati.
ms.assetid: 4e819975-84a5-4b73-9a19-792d3607da9c
title: Funzione GetStringsFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringsFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 25fbc149a663ef68d1588218937568401f414ef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966459"
---
# <a name="getstringsfromblob-function"></a>GetStringsFromBlob (funzione)

La funzione **GetStringsFromBlob** USA chiamate sequenziali per recuperare tutte le stringhe all'interno degli intervalli specificati.

## <a name="syntax"></a>Sintassi


```C++
DWORD GetStringsFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pRequestedOwnerName,
  _In_  const char  *pRequestedCategoryName,
  _In_  const char  *pRequestedTagName,
  _Out_ const char  **ppReturnedOwnerName,
  _Out_ const char  **ppReturnedCategoryName,
  _Out_ const char  **ppReturnedTagName,
  _Out_ const char  **ppReturnedString,
  _Out_       DWORD *pRestartKey
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hBlob* \[ in\]
</dt> <dd>

Handle per il BLOB.

</dd> <dt>

*pRequestedOwnerName* \[ in\]
</dt> <dd>

Puntatore alla sezione del proprietario da cui ottenere la stringa.

</dd> <dt>

*pRequestedCategoryName* \[ in\]
</dt> <dd>

Puntatore alla sezione della categoria da cui ottenere la stringa.

</dd> <dt>

*pRequestedTagName* \[ in\]
</dt> <dd>

Puntatore al tag per la stringa richiesta.

</dd> <dt>

*ppReturnedOwnerName* \[ out\]
</dt> <dd>

Puntatore alla variabile che punta alla posizione in cui verrà restituito il nome del **proprietario** .

</dd> <dt>

*ppReturnedCategoryName* \[ out\]
</dt> <dd>

Puntatore alla variabile che punta alla posizione in cui verrà restituito il nome della **categoria** .

</dd> <dt>

*ppReturnedTagName* \[ out\]
</dt> <dd>

Puntatore alla variabile che punta alla posizione in cui verrà restituito il nome del **tag** .

</dd> <dt>

*ppReturnedString* \[ out\]
</dt> <dd>

Puntatore alla variabile che punta alla posizione in cui verrà restituito il nome della stringa.

</dd> <dt>

*pRestartKey* \[ out\]
</dt> <dd>

Puntatore alla variabile in cui verrà specificata e restituita la chiave di riavvio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica il problema.

Se una combinazione specificata di informazioni su **proprietario**, **categoria** e **tag** non esiste, il valore restituito è NMERR la voce del **BLOB non \_ \_ \_ \_ \_ esiste**.

Quando il BLOB viene attraversato completamente entro i limiti specificati inizialmente, la funzione restituisce la **voce del \_ BLOB NMERR non \_ \_ \_ \_ esiste** e il parametro *pRestartKey* punta a zero.

## <a name="remarks"></a>Commenti

Nella chiamata iniziale alla funzione **GetStringsFromBlob** , il parametro *pRestartKey* punta a una variabile che contiene il valore zero. I parametri preesistenti possono essere utilizzati solo quando la *chiave di riavvio* è zero. Nelle chiamate successive, quando *pRestartKey* ha valori diversi da zero, i parametri *precercati* vengono ignorati. Nella chiamata iniziale, all può puntare a **null**, che imposta la query in modo che restituisca tutte le voci nel BLOB, una per ogni chiamata successiva.

La specifica di un proprietario limita le stringhe restituite solo a tale proprietario. Una limitazione simile è vera per le categorie e i tag, con l'avvertenza aggiuntiva che se viene specificata una categoria, è necessario specificare anche un proprietario e se viene specificato un tag, è necessario specificare una categoria (e quindi un proprietario).

Quando viene restituita la chiamata iniziale a **GetStringsFromBlob** , *pRestartKey* punta a un nuovo valore, che deve essere specificato nella chiamata successiva alla funzione per ottenere il valore successivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[SetStringInBlob](setstringinblob.md)
</dt> <dt>

[GetBoolFromBlob](getboolfromblob.md)
</dt> <dt>

[GetClassIDFromBlob](getclassidfromblob.md)
</dt> <dt>

[GetDwordFromBlob](getdwordfromblob.md)
</dt> <dt>

[GetMacAddressFromBlob](getmacaddressfromblob.md)
</dt> <dt>

[GetNetworkInfoFromBlob](getnetworkinfofromblob.md)
</dt> <dt>

[GetNPPAddressFilterFromBlob](getnppaddressfilterfromblob.md)
</dt> <dt>

[GetNPPPatternFilterFromBlob](getnpppatternfilterfromblob.md)
</dt> <dt>

[GetNPPTriggerFromBlob](getnpptriggerfromblob.md)
</dt> <dt>

[GetStringFromBlob](getstringfromblob.md)
</dt> </dl>

 

 




