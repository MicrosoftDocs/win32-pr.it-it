---
description: Imposta una specifica Microsoft .NET'opzione di accesso Passport.
ms.assetid: 5ec79faa-1c74-42a4-b964-ea15edacda79
title: Metodo IPassportManager3::p ut_Option
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.put_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 92a1c432df3f3948a85205e26da64073722ba84dd365ebdcaccf3b80521c517c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827212"
---
# <a name="ipassportmanager3put_option-method"></a>Metodo IPassportManager3::p ut \_ Option

Imposta una specifica Microsoft .NET'opzione di accesso Passport.

> [!Note]  
> Il **metodo \_ put Option** appartiene all'interfaccia [**IPassportManager3.**](/previous-versions/ms817681(v=msdn.10)) Questo argomento integra la documentazione iniziale.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Option(
   BSTR    name,
   VARIANT newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nome* 
</dt> <dd>

Opzione di accesso da impostare. Attualmente, l'unica opzione supportata è iMode.

</dd> <dt>

*newVal* 
</dt> <dd>

VARIANT  (VT \_ BOOL) che specifica il nuovo valore per l'opzione. Questo valore può essere True o False.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK quando il metodo ha esito positivo.

## <a name="remarks"></a>Commenti

Questo metodo viene fornito con le versioni precedenti di Passport SDK.

 

 
