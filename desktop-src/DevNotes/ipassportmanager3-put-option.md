---
description: Imposta un'opzione di accesso Microsoft .NET Passport specifica.
ms.assetid: 5ec79faa-1c74-42a4-b964-ea15edacda79
title: IPassportManager3::p ut_Option metodo
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
ms.openlocfilehash: 52a1324c4b1a04a207b5bccac1a95bcd060be8ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965928"
---
# <a name="ipassportmanager3put_option-method"></a>IPassportManager3: \_ Metodo Option ut:p

Imposta un'opzione di accesso Microsoft .NET Passport specifica.

> [!Note]  
> Il metodo **put \_ Option** appartiene all'interfaccia [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) . Questo argomento integra la documentazione iniziale.

 

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

**Variant** (VT \_ bool) che specifica il nuovo valore per l'opzione. Questo valore può essere true o false.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK quando il metodo ha esito positivo.

## <a name="remarks"></a>Commenti

Questo metodo viene fornito con le versioni precedenti di Passport SDK.

 

 
