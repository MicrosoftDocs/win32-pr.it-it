---
title: Metodo IGatherNotify init (deprecated)
description: Questo argomento dell'interfaccia di ricerca desktop di Windows è deprecato e viene sostituito dall'API di ricerca di Windows ISearchPersistentItemsChangedSink nel Windows SDK. | Metodo IGatherNotify init (deprecated)
ms.assetid: 6a5f89eb-10f4-4262-89bf-b47e345f12eb
keywords:
- Metodo Init (deprecated) ambiente Windows legacy
- Metodo Init (deprecated) Windows legacy environment features, interfaccia IGatherNotify
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IGatherNotify, metodo init (deprecated)
topic_type:
- apiref
api_name:
- IGatherNotify.Init (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81379bb4a9a7c6099912bfc9ebca170141d76cd2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321613"
---
# <a name="igathernotifyinit-deprecated-method"></a>Metodo IGatherNotify:: init (deprecated)

\[**Init** può essere modificato o non disponibile nelle versioni successive del sistema operativo o del prodotto.\]

Questo argomento dell'interfaccia di ricerca desktop di Windows è deprecato e viene sostituito dall'API di ricerca di Windows [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) nel Windows SDK.

Inizializza l'interfaccia del Gatherer. Consente inoltre di specificare l'indice da notificare e l'archivio applicazioni da monitorare.

## <a name="syntax"></a>Sintassi


```C++
void Init (Deprecated)(
  [in] BSTR    bstrApplication,
  [in] BSTR    bstrProject,
  [in] variant varScopesBstrArray
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrApplication* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Stringa che specifica l'applicazione di destinazione.

</dd> <dt>

*bstrProject* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Stringa che specifica il nome dell'indicizzatore a cui passare le informazioni del Gatherer.

</dd> <dt>

*varScopesBstrArray* \[ in\]
</dt> <dd>

Tipo: **Variant**

Parametro facoltativo che consente di passare una matrice di ambiti da inizializzare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Inizializzare con Application = "RSApp", Project = "SetIndex".

 

 
