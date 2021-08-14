---
title: Funzione DsRestorePrepare (Ntdsbcli.h)
description: Si connette al server di directory specificato e lo prepara per l'operazione di ripristino.
ms.assetid: e847d57a-32e1-49c0-800c-7ce0e5f442fa
ms.tgt_platform: multiple
keywords:
- Funzione DsRestorePrepare in Active Directory
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
ms.openlocfilehash: f11b844919cc459788bbd8acda722a68344ae16807e45be9bd6dcd5780b09d6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191807"
---
# <a name="dsrestoreprepare-function"></a>Funzione DsRestorePrepare

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire Windows Vista, [usare Servizio Copia Shadow del volume (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

La **funzione DsRestorePrepare** si connette al server di directory specificato e la prepara per l'operazione di ripristino.

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

*szServerName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null contenente il nome del server da ripristinare. Le barre rovesciate precedenti sono facoltative. Il server deve essere lo stesso computer da cui viene chiamata questa funzione. Il nome del server non può contenere caratteri di sottolineatura ( \_ ). Un esempio di nome di server è \\ \\ "server1".

</dd> <dt>

*rtFlag* \[ Pollici\]
</dt> <dd>

Specifica il tipo di ripristino da eseguire. Può essere zero o uno dei valori seguenti.

<dt>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**RESTORE \_ TYPE \_ CATCHUP**


</dt> <dd>

Valore predefinito. La versione ripristinata viene riconciliata tramite la logica di riconciliazione standard in modo che il DIT ripristinato possa essere sincronizzato con altri computer server aziendali.

</dd> <dt>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**RESTORE \_ TYPE \_ AUTHORATATIVE**


</dt> <dd>

Non supportato.

</dd> <dt>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**TIPO \_ DI RIPRISTINO \_ ONLINE**


</dt> <dd>

Non supportato. Il ripristino viene eseguito quando NTDS è online.

</dd> </dl> </dd> <dt>

*pvExpiryToken* \[ Pollici\]
</dt> <dd>

Puntatore al token di scadenza associato al backup da ripristinare. Questo token è stato ottenuto dalla [**funzione DsBackupPrepare**](dsbackupprepare.md) quando è stato eseguito il backup della directory.

Se questo parametro è **NULL,** l'handle restituito in *phbc* può essere usato solo per ottenere le directory di ripristino con [**la funzione DsRestoreGetDatabaseLocations.**](dsrestoregetdatabaselocations.md) L'handle non può essere usato per altre funzioni di ripristino.

</dd> <dt>

*cbExpiryTokenSize* \[ Pollici\]
</dt> <dd>

Contiene le dimensioni, in byte, del token di scadenza in *pvExpiryToken.*

</dd> <dt>

*phbc* \[ Cambio\]
</dt> <dd>

Puntatore a **un valore HBC** che riceve l'handle per il ripristino. Questo handle viene usato quando si chiamano altre funzioni di ripristino del servizio directory, ad esempio [**DsBackupOpenFile**](dsbackupopenfile.md) [**e DsRestoreEnd.**](dsrestoreend.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, restituisce codici **HRESULT** standard. In caso contrario, viene restituito un codice di errore.

## <a name="remarks"></a>Commenti

La **funzione DsRestorePrepare** richiede che il chiamante sia membro del gruppo Administrators nel server.

**DsRestorePrepare** può essere usato con o senza un token fornito. Se il token viene fornito, viene verificata la scadenza e tutte le operazioni sono consentite nel contesto restituito. Se il token non viene fornito, il contesto restituito è limitato e può essere usato solo per la [**funzione DsRestoreGetDatabaseLocations.**](dsrestoregetdatabaselocations.md) Non può essere usato per la [**funzione DsRestoreRegister.**](dsrestoreregister.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DsRestorePrepareW** (Unicode) e **DsRestorePrepareA** (ANSI)<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Ripristino di un server Active Directory](restoring-an-active-directory-server.md)
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

 

