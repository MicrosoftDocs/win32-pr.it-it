---
title: WM/MCDI
description: L'attributo WM/MCDI contiene l'identificatore del CD musicale. Si tratta di un dump binario del sommario del CD usato per identificare in modo univoco il CD.
ms.assetid: cb16c62b-b9e0-4676-b1bb-ff26a2e09cb7
keywords:
- Formato di Windows Media WM/MCDI
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da5c629bcef9ca2072d0ddda433fde97932e97e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299222"
---
# <a name="wmmcdi"></a>WM/MCDI

L'attributo **WM/MCDI** contiene l'identificatore del CD musicale. Si tratta di un dump binario del sommario del CD usato per identificare in modo univoco il CD.

## <a name="global-constant"></a>Costante globale

g \_ wszWMMCDI

## <a name="data-type"></a>Tipo di dati

**\_binario di tipo WMT \_**

## <a name="remarks"></a>Commenti

Questo attributo è compatibile con il frame ID3, MCDI. Per la specifica ID3 per il frame MCDI è necessario che esista un solo frame per ogni file e che esista un frame TRCK valido. L'editor dei metadati non esegue alcuna convalida per queste regole. Inoltre, le dimensioni di WM/MCDI non sono limitate a 804 byte, così come il frame ID3 MCDI.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




