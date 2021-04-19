---
title: Struttura TF_RENDERINGMARKUP
description: La \_ struttura della struttura TF RENDERINGMARKUP contiene un intervallo e le informazioni sugli attributi di visualizzazione.
ms.assetid: 206e679b-f2eb-4f28-ac2a-58f3c222a020
keywords:
- Framework servizi di testo struttura TF_RENDERINGMARKUP
topic_type:
- apiref
api_name:
- TF_RENDERINGMARKUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 166a60182ae7b53dbc70993a7bae81991e42255b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299067"
---
# <a name="tf_renderingmarkup-structure"></a>\_Struttura RENDERINGMARKUP TF

La struttura della struttura [**tf \_ RENDERINGMARKUP**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) contiene un intervallo e le informazioni sugli attributi di visualizzazione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  ITfRange*           pRange;
  TF_DISPLAYATTRIBUTE tfDisplayAttr;
} TF_RENDERINGMARKUP;
```



## <a name="members"></a>Members

<dl> <dt>

**pRange**
</dt> <dd>

Puntatore a un'interfaccia [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) .

</dd> <dt>

**tfDisplayAttr**
</dt> <dd>

Visualizzare le informazioni sugli attributi.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura non è attualmente presente nei file di intestazione pubblici. Per usare questa API, è necessario compilare MIDL per il [prototipo](prototypes.md).

 

 




