---
description: Imposta o recupera i dati da firmare. Si tratta della proprietà predefinita.
ms.assetid: 554ca500-403d-4c2a-868e-9e635d0b358e
title: Proprietà SignedData. Content
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3c2ac97eeee317b4ec170338f666e5b5d9277861
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332834"
---
# <a name="signeddatacontent-property"></a>Proprietà SignedData. Content

\[La proprietà **Content** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La proprietà **Content** imposta o recupera i dati da firmare. Si tratta della proprietà predefinita.

## <a name="syntax"></a>Sintassi


```VB
SignedData.Content As String
```



## <a name="property-value"></a>Valore proprietà

Dati da firmare.

## <a name="remarks"></a>Commenti

Questa proprietà deve essere inizializzata prima che venga chiamato il metodo [**Sign**](signeddata-sign.md) . Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero [*stato*](../secgloss/s-gly.md) dell'oggetto e tutte le firme associate all'oggetto prima della modifica della proprietà vengono perse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
