---
description: Questa funzione accetta l'attributo Origin se presente dal token Origin e li imposta su un duplicato del token che eredita e restituisce il token duplicato.
ms.assetid: ED1FAEA1-0665-49FA-BD8B-232254B4C883
title: srpInheritOriginClaim (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- srpInheritOriginClaim
api_type:
- DllExport
api_location:
- srpapi.dll
ms.openlocfilehash: 3edf274622bc1a2611bc49d710a809bd80bd501a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306421"
---
# <a name="srpinheritoriginclaim-function"></a>srpInheritOriginClaim (funzione)

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Questa funzione accetta l'attributo Origin se presente dal token Origin e li imposta su un duplicato del token che eredita e restituisce il token duplicato. Il chiamante può quindi rappresentare il token restituito. A questa funzione non è associata alcuna libreria di importazione. È necessario utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a srpapi.dll.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI srpInheritOriginClaim(
  _In_ Handle OriginToken,
  _In_ Handle InheritingToken,
       Handle ResultToken
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OriginToken* \[ in\]
</dt> <dd>

Handle per il token duplicato e che riceve l'attributo Origin ereditato. Questo handle deve essere aperto con il \_ diritto di accesso duplicato del token.

</dd> <dt>

*InheritingToken* \[ in\]
</dt> <dd>

Handle per il token duplicato e che riceve l'attributo Origin ereditato. Questo handle deve essere aperto con il \_ diritto di accesso duplicato del token. 

</dd> <dt>

*ResultToken* 
</dt> <dd>

Se l'operazione riesce, riceve il token duplicato. Il chiamante può rappresentarlo per eseguire operazioni con l'attributo Origin ereditato. Il chiamante acquisisce la proprietà di questo handle e deve chiuderlo. 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Srpapi.dll</dt> </dl> |



 

