---
description: 'Metodo IXml2Dex::WriteXMLPart : non implementato.'
ms.assetid: d0fc571f-79f5-448a-8082-6e5f7f48118f
title: Metodo IXml2Dex::WriteXMLPart
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: a9ca563c0c780b9c2f4d2171fdaa9e365b15a3b014ec4c4a42a28de7b43f3f3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397562"
---
# <a name="ixml2dexwritexmlpart-method"></a>Metodo IXml2Dex::WriteXMLPart

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Non implementato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WriteXMLPart(
   IUnknown *pTimeline,
   double   dStart,
   double   dEnd,
   BSTR     FileName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTimeline* 
</dt> <dd>

Riservato.

</dd> <dt>

*dStart* 
</dt> <dd>

Riservato.

</dd> <dt>

*dEnd* 
</dt> <dd>

Riservato.

</dd> <dt>

*FileName* 
</dt> <dd>

Riservato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IXml2Dex**](ixml2dex.md)
</dt> </dl>

 

 



