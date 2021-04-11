---
title: Funzione DsRestorePrepare (ntdsbcli. h)
description: Si connette al server di directory specificato e lo prepara per l'operazione di ripristino.
ms.assetid: e847d57a-32e1-49c0-800c-7ce0e5f442fa
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsRestorePrepare
topic_type:
- apiref
api_name:
- DsRestorePrepare
- DsRestorePrepareA
- DsRestorePrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb040a315b6cc94f2d296b032a954b00473a4ca2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119606"
---
# <a name="dsrestoreprepare-function"></a>DsRestorePrepare (funzione)

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

La funzione **DsRestorePrepare** si connette al server di directory specificato e la prepara per l'operazione di ripristino.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DsRestorePrepare(
  _In_  LPCWSTR szServerName,
  _In_  ULONG   rtFlag,
  _In_  PVOID   pvExpiryToken,
  _In_  DWORD   cbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szServerName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il nome del server da ripristinare. Le barre rovesciate precedenti sono facoltative. Il server deve essere lo stesso computer da cui viene chiamata la funzione. Il nome del server non può contenere caratteri di sottolineatura ( \_ ). Un esempio di nome di server è " \\ \\ Server1".

</dd> <dt>

*rtFlag* \[ in\]
</dt> <dd>

Specifica il tipo di ripristino da eseguire. Può essere zero o uno dei valori seguenti.

<dt>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**tipo di ripristino \_ \_ Catchup**


</dt> <dd>

Valore predefinito. La versione ripristinata viene riconciliata attraverso la logica di riconciliazione standard, in modo che il DIT ripristinato possa essere sincronizzato con altri computer server aziendali.

</dd> <dt>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**tipo di ripristino \_ \_ AUTHORATATIVE**


</dt> <dd>

Non supportato.

</dd> <dt>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**tipo di ripristino \_ \_ online**


</dt> <dd>

Non supportato. Il ripristino viene eseguito quando NTDS è online.

</dd> </dl> </dd> <dt>

*pvExpiryToken* \[ in\]
</dt> <dd>

Puntatore al token di scadenza associato al backup da ripristinare. Questo token è stato ottenuto dalla funzione [**DsBackupPrepare**](dsbackupprepare.md) quando è stato eseguito il backup della directory.

Se questo parametro è **null**, l'handle restituito in *phbc* può essere utilizzato solo per ottenere le directory di ripristino con la funzione [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) . Non è possibile usare l'handle per altre funzioni di ripristino.

</dd> <dt>

*cbExpiryTokenSize* \[ in\]
</dt> <dd>

Contiene la dimensione, in byte, del token di scadenza in *pvExpiryToken*.

</dd> <dt>

*phbc* \[ out\]
</dt> <dd>

Puntatore a un valore **HBC** che riceve l'handle per il ripristino. Questo handle viene utilizzato per chiamare altre funzioni di ripristino del servizio directory, ad esempio [**DsBackupOpenFile**](dsbackupopenfile.md) e [**DsRestoreEnd**](dsrestoreend.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, restituisce un codice **HRESULT** standard; in caso contrario, viene restituito un codice di errore.

## <a name="remarks"></a>Commenti

La funzione **DsRestorePrepare** richiede che il chiamante sia un membro del gruppo Administrators nel server.

**DsRestorePrepare** può essere usato con o senza un token fornito. Se il token viene fornito, viene verificata la scadenza e tutte le operazioni sono consentite nel contesto restituito. Se il token non viene specificato, il contesto restituito viene limitato e può essere usato solo per la funzione [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) . Non può essere usata per la funzione [**DsRestoreRegister**](dsrestoreregister.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DsRestorePrepareW** (Unicode) e **DsRestorePrepareA** (ANSI)<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Ripristino di un server di Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> <dt>

[**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md)
</dt> <dt>

[**DsRestoreEnd**](dsrestoreend.md)
</dt> </dl>

 

