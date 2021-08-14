---
title: Metodo IGatherNotify Init (deprecato)
description: Questo Windows dell'interfaccia di Desktop Search è deprecato e viene sostituito dall'API ISearchPersistentItemsChangedSink di Windows Search nell'SDK Windows. | Metodo IGatherNotify Init (deprecato)
ms.assetid: 6a5f89eb-10f4-4262-89bf-b47e345f12eb
keywords:
- Metodo Init (deprecato) Legacy Windows Environment Features
- Metodo Init (deprecato) Legacy Windows Environment Features , interfaccia IGatherNotify
- Interfaccia IGatherNotify Legacy Windows environment features , Metodo Init (deprecato)
topic_type:
- apiref
api_name:
- IGatherNotify.Init (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: db5666197524afb454927036cdd68375dfb2937197ed211646b63d80a09e5b12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359301"
---
# <a name="igathernotifyinit-deprecated-method"></a>Metodo IGatherNotify::Init (deprecato)

\[**Init** può essere modificato o non disponibile nelle versioni successive del sistema operativo o del prodotto.\]

Questo Windows'interfaccia di Desktop Search è deprecato e viene sostituito dall'API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) di Windows Search nell'SDK Windows.

Inizializza l'interfaccia Gatherer. Specifica anche l'indice da notificare e l'archivio applicazioni da monitorare.

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

*bstrApplication* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Stringa che specifica l'applicazione di destinazione.

</dd> <dt>

*bstrProject* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Stringa che specifica il nome dell'indicizzatore a cui passare le informazioni sul gatherer.

</dd> <dt>

*varScopesBstrArray* \[ Pollici\]
</dt> <dd>

Tipo: **variante**

Parametro facoltativo che consente di passare una matrice di ambiti da inizializzare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Inizializzare con application="RSApp", Project="MyIndex".

 

 
