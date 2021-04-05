---
description: Recupera il valore di una proprietà del provider specificata.
ms.assetid: 69235520-acaa-4ec4-9fd6-4b3297e14376
title: Funzione SslGetProviderProperty (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetProviderProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ced0f32d45531a1220f7aae9fe0e660648e5d1bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884310"
---
# <a name="sslgetproviderproperty-function"></a>SslGetProviderProperty (funzione)

La funzione **SslGetProviderProperty** Recupera il valore di una proprietà del provider specificata.

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslGetProviderProperty(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _In_    LPCWSTR            pszProperty,
  _Out_   PBYTE              ppbOutput,
  _Out_   DWORD              *pcbOutput,
  _Inout_ PVOID              *ppEnumState,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ in\]
</dt> <dd>

Handle del provider di [*protocollo Secure Sockets Layer*](/windows/desktop/SecGloss/s-gly) (SSL) per il quale recuperare la proprietà.

</dd> <dt>

*pszProperty* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione null che contiene il nome della proprietà da recuperare.

</dd> <dt>

*ppbOutput* \[ out\]
</dt> <dd>

Indirizzo di un buffer che riceve il valore della proprietà.

Il chiamante della funzione deve liberare questo buffer chiamando la funzione [**SslFreeBuffer**](sslfreebuffer.md) .

</dd> <dt>

*pcbOutput* \[ out\]
</dt> <dd>

Dimensione, in byte, del buffer *pbOutput* .

</dd> <dt>

*ppEnumState* \[ in uscita\]
</dt> <dd>

Indirizzo di un puntatore **void** che riceve le informazioni sullo stato di enumerazione utilizzate nelle chiamate successive a questa funzione. Queste informazioni hanno significato solo per il provider SSL ed è opaca per il chiamante. Il provider SSL usa queste informazioni per determinare l'elemento successivo nell'enumerazione. Se la variabile a cui punta questo parametro contiene **null**, l'enumerazione viene avviata dall'inizio.

Il chiamante della funzione deve liberare la memoria chiamando la funzione [**SslFreeBuffer**](sslfreebuffer.md) .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ Nessun \_**</dt> <dt>0x8009000EL</dt> di memoria </dl>         | La memoria disponibile non è sufficiente per allocare i buffer necessari.<br/> |
| <dl> <dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt> </dl>    | Handle *hSslProvider* non valido.<br/>                       |
| <dl> <dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt> </dl> | Uno dei parametri specificati non è valido.<br/>                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

