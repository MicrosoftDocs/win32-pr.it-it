---
description: Ottiene un oggetto decodificatore, se ne esiste uno.
ms.assetid: b8a1c7c9-e7ac-4b0e-a342-5b923ab83df3
title: Metodo EncodedData. decoder
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Decoder
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 334895ed683d0c582628b4b623a7343ca561be22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331423"
---
# <a name="encodeddatadecoder-method"></a>Metodo EncodedData. decoder

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Il metodo **decodificatore** ottiene un oggetto decodificatore, se ne esiste uno.

## <a name="syntax"></a>Sintassi


```VB
EncodedData.Decoder()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="remarks"></a>Commenti

Se i dati codificati non dispongono di un oggetto Decoder, viene restituito **null** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
