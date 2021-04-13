---
title: WM/Track
description: L'attributo WM/Track contiene il numero di traccia del contenuto. Questo attributo è in base zero ed è supportato per la compatibilità con le versioni precedenti. Il nuovo contenuto deve invece usare l'attributo WM/numero.
ms.assetid: c763d7b0-9d12-4a4e-8c9f-9cf67bd2a02b
keywords:
- WM/Track Windows Media Format
topic_type:
- apiref
api_name:
- WM/Track
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 244426175ea74bc0281f8822964c2fc0bfa37aa7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397163"
---
# <a name="wmtrack"></a>WM/Track

L'attributo **WM/Track** contiene il numero di traccia del contenuto. Questo attributo è in base zero ed è supportato per la compatibilità con le versioni precedenti. Il nuovo contenuto deve invece usare l'attributo [**WM/numero**](wm-tracknumber.md) .

## <a name="global-constant"></a>Costante globale

g \_ wszWMTrack

## <a name="data-type"></a>Tipo di dati

**\_stringa di tipo WMT \_**

## <a name="remarks"></a>Commenti

Molte applicazioni esistenti scrivono il valore per **WM/Track** come **DWORD**. Se si crea un'applicazione che riproduce file da origini sconosciute, è necessario includere il codice per gestire i valori stringa e **DWORD** .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




