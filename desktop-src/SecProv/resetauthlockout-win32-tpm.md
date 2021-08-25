---
description: Reimposta il periodo di timeout o un altro meccanismo implementato dai produttori TPM per la protezione dagli attacchi al dizionario sui valori di autorizzazione TPM.
ms.assetid: c2fba6a2-2d03-4ffd-9841-4a9eac0a20ac
title: Metodo ResetAuthLockOut della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetAuthLockOut
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 779ae7e8578019215e0bab1091512c64d68a84675d702ea7a0d8a5c37e8f081f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906301"
---
# <a name="resetauthlockout-method-of-the-win32_tpm-class"></a>Metodo ResetAuthLockOut della classe Tpm Win32 \_

Il **metodo ResetAuthLockOut** della classe [**\_ Tpm Win32**](win32-tpm.md) reimposta il periodo di timeout o un altro meccanismo implementato dai produttori TPM per la protezione dagli attacchi del dizionario ai valori di autorizzazione TPM. In un attacco con dizionario, un utente malintenzionato tenta di indovinare un valore di autorizzazione TPM corretto provando in modo esaustivo tutti i valori possibili.

Usare questo metodo se il TPM è bloccato a causa di troppi tentativi non corretti di immissione dell'autorizzazione del proprietario o di altri valori di autorizzazione. Quando il TPM è bloccato, alcuni o tutti i comandi emessi al TPM restituiranno un errore, TPM \_ E DEFEND LOCK RUNNING \_ \_ \_ (0x80280803).

> [!Note]  
> Questo metodo può essere usato solo una volta sola quando il TPM è bloccato. Se l'autorizzazione del proprietario fornita a questo metodo non è corretta, il TPM si blocchi per l'intero periodo di timeout e altri tentativi di reimpostazione del blocco avranno esito negativo.

 

## <a name="syntax"></a>Sintassi


```mof
uint32 ResetAuthLockOut(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OwnerAuth* \[ in, facoltativo\]
</dt> <dd>

Tipo: **stringa**

Stringa che identifica il proprietario del TPM.

Questa stringa deve essere una stringa con terminazione Null con codifica Base64 che contiene esattamente 20 byte di dati binari. Usare il [**metodo ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) per convertire una passphrase nel formato previsto. Il *parametro OwnerAuth* viene letto dal Registro di sistema se non ne viene fornito nessuno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

È possibile restituire tutti gli errori TPM e gli errori specifici dei servizi di base TPM. Nella tabella seguente sono elencati alcuni dei valori restituiti comuni.



| Codice/valore restituito                                                                                                                                                            | Descrizione                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                            | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                                                     |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl> | Il valore di autorizzazione del proprietario specificato non è corretto. Altri tentativi di reimpostazione del blocco avranno esito negativo con lo stesso errore. Attendere la scadenza del periodo di timeout o di un altro meccanismo specifico del produttore prima di riprovare a eseguire i comandi TPM bloccati.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il comando \_ TPM ResetLockValue nel TPM. Il comportamento esatto di questo metodo varia tra i produttori di TPM. La documentazione del produttore del computer o del TPM può fornire informazioni aggiuntive sull'implementazione del meccanismo di attacco anti-dizionario.

In generale, i produttori possono rilevare gli attacchi al dizionario tenendo traccia delle autenticazioni non riuscite. Se il numero o la frequenza degli errori diventa sufficientemente elevata, il TPM blocchi altri comandi per un determinato periodo di tempo. In genere, il periodo di timeout iniziale sarà breve, per consentire a un utente legittimo di correggere la situazione. Se gli errori continuano, la durata di ogni periodo di timeout successivo può aumentare rapidamente.

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                      |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
