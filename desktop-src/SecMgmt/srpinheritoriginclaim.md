---
description: Questa funzione accetta l'attributo di origine, se presente, dal token di origine e li imposta su un duplicato del token che eredita e restituisce il token duplicato.
ms.assetid: ED1FAEA1-0665-49FA-BD8B-232254B4C883
title: Funzione srpInheritOriginClaim
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
ms.openlocfilehash: 64436c699f5cb24b2a12675342078242a340fb2e53de3a6a8f3224d8b88beac0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004888"
---
# <a name="srpinheritoriginclaim-function"></a>Funzione srpInheritOriginClaim

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Questa funzione accetta l'attributo di origine, se presente, dal token di origine e li imposta su un duplicato del token che eredita e restituisce il token duplicato. Il chiamante può quindi rappresentare il token restituito. A questa funzione non è associata alcuna libreria di importazione. È necessario usare le [**funzioni LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi in modo dinamico srpapi.dll.

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

*OriginToken* \[ Pollici\]
</dt> <dd>

Handle per il token duplicato che riceve l'attributo di origine ereditato. Questo handle deve essere aperto con il diritto di accesso TOKEN \_ DUPLICATE.

</dd> <dt>

*InheritingToken* \[ Pollici\]
</dt> <dd>

Handle per il token duplicato che riceve l'attributo di origine ereditato. Questo handle deve essere aperto con il diritto di accesso TOKEN \_ DUPLICATE. 

</dd> <dt>

*ResultToken* 
</dt> <dd>

In caso di esito positivo, riceve il token duplicato. Il chiamante può rappresentarlo per eseguire operazioni con l'attributo di origine ereditato. Il chiamante assume la proprietà di questo handle e deve chiuderlo. 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                           |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Srpapi.dll</dt> </dl> |



 

