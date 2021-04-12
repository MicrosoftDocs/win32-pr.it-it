---
title: Metodo IGatherNotify AddScope (deprecato)
description: Questo argomento dell'interfaccia di ricerca desktop di Windows è deprecato e viene sostituito dall'API di ricerca di Windows ISearchPersistentItemsChangedSink nel Windows SDK. | Metodo IGatherNotify AddScope (deprecato)
ms.assetid: 3b250818-1876-40b2-9a85-91f2bf6f52ec
keywords:
- Metodo AddScope (deprecato) funzionalità dell'ambiente Windows legacy
- Metodo AddScope (deprecato) funzionalità dell'ambiente Windows legacy, interfaccia IGatherNotify
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IGatherNotify, metodo AddScope (deprecato)
topic_type:
- apiref
api_name:
- IGatherNotify.AddScope (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 967dc4f30acee2f8d8adbcfec04f0508e53bba15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353011"
---
# <a name="igathernotifyaddscope-deprecated-method"></a>Metodo IGatherNotify:: AddScope (deprecato)

\[**AddScope** può essere modificato o non disponibile nelle versioni successive del sistema operativo o del prodotto.\]

Questo argomento dell'interfaccia di ricerca desktop di Windows è deprecato e viene sostituito dall'API di ricerca di Windows [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) nel Windows SDK.

Aggiunge la pagina iniziale o l'URL che si sta monitorando. Viene avviata una ricerca per indicizzazione incrementale quando si esegue la connessione e si presuppone che tutte le altre modifiche apportate all'URL siano notificate

## <a name="syntax"></a>Sintassi


```C++
void AddScope (Deprecated)(
  [in] BSTR bstrScope
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrScope* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Stringa che specifica la pagina iniziale o URL che si sta monitorando.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La chiamata a questo metodo avvia una ricerca per indicizzazione incrementale quando si è connessi all'archivio. In seguito si presuppone che tutte le modifiche apportate all'URL siano notificate dopo l'aggiornamento iniziale.

 

 
