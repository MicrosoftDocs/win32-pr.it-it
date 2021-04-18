---
description: Codifica una stringa come Base64.
ms.assetid: 73a279e3-40b0-4db8-89d3-95627f0878dd
title: Utilities. Base64Encode, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Encode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0536097e3e46fcc09702c1e4000d2fbd9856c205
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326887"
---
# <a name="utilitiesbase64encode-method"></a>Utilities. Base64Encode, metodo

\[Il metodo **Base64Encode** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.\]

Il metodo **Base64Encode** codifica una stringa come Base64.

## <a name="syntax"></a>Sintassi


```VB
Utilities.Base64Encode( _
  ByVal SrcString _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SrcString* \[ in\]
</dt> <dd>

Stringa da codificare come Base64.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Stringa con codifica Base64.

## <a name="remarks"></a>Commenti

La codifica Base64 è lo schema utilizzato per la trasmissione di dati binari. Base64 elabora i dati come gruppi a 24 bit, eseguendo il mapping di questi dati a quattro caratteri codificati. La codifica Base64 viene a volte definita codifica da 3 a 4. Ogni 6 bit del gruppo a 24 bit viene utilizzato come indice in una tabella di mapping (alfabeto Base64) per ottenere un carattere per i dati codificati. I dati codificati hanno lunghezze di riga limitate a 76 caratteri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Utilità**](utilities.md)
</dt> </dl>

 

 




