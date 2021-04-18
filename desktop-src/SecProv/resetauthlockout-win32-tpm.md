---
description: Reimposta il periodo di timeout o un altro meccanismo che i produttori di TPM implementano per proteggere da attacchi con dizionario sui valori di autorizzazione TPM.
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
ms.openlocfilehash: d28287e410fbaf65ce5b1e617113c35cfece160b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306377"
---
# <a name="resetauthlockout-method-of-the-win32_tpm-class"></a>Metodo ResetAuthLockOut della \_ classe TPM Win32

Il metodo **ResetAuthLockOut** della classe [**\_ TPM Win32**](win32-tpm.md) Reimposta il periodo di timeout o un altro meccanismo che i produttori di TPM implementano per proteggere da attacchi con dizionario sui valori di autorizzazione TPM. In un attacco con dizionario, un utente malintenzionato tenta di indovinare un valore di autorizzazione TPM corretto ritentando in modo esaustivo tutti i valori possibili.

Utilizzare questo metodo se il TPM è bloccato a causa di un numero eccessivo di tentativi non corretti di immissione dell'autorizzazione del proprietario o di altri valori di autorizzazione. Quando il TPM è bloccato, alcuni o tutti i comandi emessi al TPM restituiscono un errore, TPM \_ E \_ difendono il \_ blocco \_ in esecuzione (0x80280803).

> [!Note]  
> Questo metodo può essere utilizzato solo una volta quando il TPM è bloccato. Se l'autorizzazione del proprietario fornita a questo metodo non è corretta, il TPM si bloccherà per l'intero periodo di timeout e i tentativi aggiuntivi di reimpostazione del blocco avranno esito negativo.

 

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

Questa stringa deve essere una stringa con codifica Base64 con terminazione null che contiene esattamente 20 byte di dati binari. Usare il metodo [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) per tradurre una passphrase nel formato previsto. Il parametro *OwnerAuth* viene letto dal registro di sistema se non ne viene specificato alcuno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM. Nella tabella seguente sono elencati alcuni dei valori restituiti comuni.



| Codice/valore restituito                                                                                                                                                            | Descrizione                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                            | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                                                     |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl> | Il valore di autorizzazione del proprietario specificato non è corretto. Ulteriori tentativi di reimpostazione del blocco avranno esito negativo con lo stesso errore. Attendere la scadenza del periodo di timeout o di un altro meccanismo specifico del produttore prima di ritentare i comandi bloccati del TPM.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il TPM \_ ResetLockValue comando sul TPM. Il comportamento esatto di questo metodo varia tra i produttori di TPM. La documentazione del produttore del computer o del TPM può fornire informazioni aggiuntive sull'implementazione del meccanismo di attacco anti-Dictionary.

In generale, i costruttori possono rilevare gli attacchi con dizionario tenendo traccia delle autenticazioni non riuscite. Se il numero o la frequenza degli errori diventa sufficientemente elevata, il TPM bloccherà altri comandi per un certo periodo di tempo. In genere, il periodo di timeout iniziale sarà breve per consentire a un utente legittimo di correggere la situazione. Se gli errori continuano, la durata di ogni periodo di timeout successivo potrebbe aumentare rapidamente.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non sono installati come parte del Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                      |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM Win32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> </dl>

 

 
