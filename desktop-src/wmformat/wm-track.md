---
title: WM/Track
description: L'attributo WM/Track contiene il numero di traccia del contenuto. Questo attributo è in base zero ed è supportato per la compatibilità con le versioni precedenti. Il nuovo contenuto deve usare invece l'attributo WM/TrackNumber.
ms.assetid: c763d7b0-9d12-4a4e-8c9f-9cf67bd2a02b
keywords:
- WM/Track windows Media Format
topic_type:
- apiref
api_name:
- WM/Track
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1113fde7b0b29b6f1f7618e9d531df83070725b9e05e70e09f64f93b027abfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026939"
---
# <a name="wmtrack"></a>WM/Track

**L'attributo WM/Track** contiene il numero di traccia del contenuto. Questo attributo è in base zero ed è supportato per la compatibilità con le versioni precedenti. Il nuovo contenuto deve usare [**invece l'attributo WM/TrackNumber.**](wm-tracknumber.md)

## <a name="global-constant"></a>Costante globale

g \_ wszWMTrack

## <a name="data-type"></a>Tipo di dati

**STRINGA DI TIPO WMT \_ \_**

## <a name="remarks"></a>Commenti

Molte applicazioni esistenti scrivono il valore **per WM/Track** come **DWORD**. Se si crea un'applicazione che riproduce file da origini sconosciute, è necessario includere il codice per gestire sia valori stringa che **valori DWORD.**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




