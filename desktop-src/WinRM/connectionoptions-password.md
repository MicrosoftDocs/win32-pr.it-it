---
title: Proprietà ConnectionOptions.Password (WSManDisp.h)
description: Imposta la password di un account locale o di dominio nel computer remoto. Questa proprietà determina la password per l'autenticazione.
ms.assetid: 61ba54b6-7da0-423e-b5b2-c4dd8aacd042
ms.tgt_platform: multiple
keywords:
- Proprietà password Windows Gestione remota
- Proprietà Password Windows gestione remota , oggetto ConnectionOptions
- Oggetto ConnectionOptions Windows gestione remota, proprietà Password
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
ms.openlocfilehash: 8ffc992b5a0560175d6562a16cf4cb3fd6bc4259eb3b712e26708dc713baba14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898991"
---
# <a name="connectionoptionspassword-property"></a>ConnectionOptions.Password - proprietà

Imposta la password di un account locale o di dominio nel computer remoto. Questa proprietà determina la password per l'autenticazione. Per altre informazioni, vedere [Autenticazione per le connessioni remote](authentication-for-remote-connections.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
ConnectionOptions.Password As String
```



## <a name="property-value"></a>Valore proprietà

Stringa contenente la password di un account locale o di dominio nel computer remoto.

Se non viene specificato alcun valore e il flag **WSManFlagCredUsernamePassword** non è impostato, viene usata la password dell'account che esegue lo script.

Se non viene specificato alcun valore e il flag **WSManFlagCredUsernamePassword** è impostato, lo script richiede all'utente di immettere la password e il nome utente, se non viene specificato. Se non vengono immessi un nome utente e una password validi, viene restituito un errore di accesso negato.

## <a name="remarks"></a>Commenti

Tenere presente che non è possibile recuperare la password. La password può essere impostata solo con questa proprietà.

Se si crea un oggetto [**ConnectionOptions**](connectionoptions.md) e si usano un nome utente e una password per connettersi Windows Remote Management, il flag **WSManFlagCredUserNamePassword** deve essere impostato nella chiamata a [**WSMan.CreateSession**](wsman-createsession.md).

Per altre informazioni sull'impostazione delle password, vedere la sezione Osservazioni in [**ConnectionOptions**](connectionoptions.md).

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene creato [**un oggetto ConnectionOptions**](connectionoptions.md) e viene impostata la **password**.


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
| Intestazione<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Connectionoptions**](connectionoptions.md)
</dt> </dl>

 

 





