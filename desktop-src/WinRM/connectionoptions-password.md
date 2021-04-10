---
title: Proprietà ConnectionOptions. password (WSManDisp. h)
description: Imposta la password di un account locale o di dominio nel computer remoto. Questa proprietà determina la password per l'autenticazione.
ms.assetid: 61ba54b6-7da0-423e-b5b2-c4dd8aacd042
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows proprietà password
- Gestione remota Windows proprietà password, oggetto ConnectionOptions
- Gestione remota Windows oggetto ConnectionOptions, proprietà password
topic_type:
- apiref
api_name:
- ConnectionOptions.Password
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4d553bf3f2a0a245e358e09a89eb1c00751e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120375"
---
# <a name="connectionoptionspassword-property"></a>Proprietà ConnectionOptions. password

Imposta la password di un account locale o di dominio nel computer remoto. Questa proprietà determina la password per l'autenticazione. Per altre informazioni, vedere [autenticazione per le connessioni remote](authentication-for-remote-connections.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
ConnectionOptions.Password As String
```



## <a name="property-value"></a>Valore proprietà

Stringa che contiene la password di un account locale o di dominio nel computer remoto.

Se non viene specificato alcun valore e il flag **WSManFlagCredUsernamePassword** non è impostato, verrà usata la password dell'account che esegue lo script.

Se non viene specificato alcun valore e viene impostato il flag **WSManFlagCredUsernamePassword** , lo script richiede all'utente di immettere la password (e il nome utente, se non viene fornito). Se non viene immesso un nome utente e una password validi, viene restituito un errore di accesso negato.

## <a name="remarks"></a>Commenti

Tenere presente che non è possibile recuperare la password. La password può essere impostata solo con questa proprietà.

Se si crea un oggetto [**ConnectionOptions**](connectionoptions.md) e si usano un nome utente e una password per connettersi a gestione remota Windows, il flag **WSManFlagCredUserNamePassword** deve essere impostato sulla chiamata a [**WSMan. CreateSession**](wsman-createsession.md).

Per ulteriori informazioni sull'impostazione delle password, vedere la sezione Osservazioni in [**ConnectionOptions**](connectionoptions.md).

## <a name="examples"></a>Esempio

L'esempio di codice seguente crea un oggetto [**ConnectionOptions**](connectionoptions.md) e imposta la **password**.


```VB
' Create a WSMan object. 
Set objWsman = CreateObject( "WSMAN.Automation" )
' Create a ConnectionOptions object
Set objOptions = objWSMan.CreateConnectionOptions
objOptions.Password = "<password>"
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





