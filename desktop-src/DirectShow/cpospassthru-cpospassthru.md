---
description: 'Costruttore CPosPassThru.CPosPassThru : metodo costruttore.'
ms.assetid: b258401c-158b-4eb8-8736-1e1ad9a8403a
title: Costruttore CPosPassThru.CPosPassThru
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CPosPassThru
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2a6c49b305b3c6638aeaaee1480d0b561fd8c99a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085599"
---
# <a name="cpospassthrucpospassthru-constructor"></a>Costruttore CPosPassThru.CPosPassThru

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin,
                   
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Puntatore al nome dell'oggetto, a scopo di debug. Allocare questo parametro nella memoria statica.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntatore al proprietario dell'oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** di aggregazione. In caso contrario, impostare questo parametro su **NULL.**

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a un **valore HRESULT.** Ignorato.

</dd> <dt>

*pPin* 
</dt> <dd>

Puntatore [**all'interfaccia IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin di input del filtro.

</dd> <dt>

 
</dt> <dd></dd> </dl>

 

 



