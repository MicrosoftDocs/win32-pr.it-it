---
description: L'azione RegisterUser registra le informazioni utente con il programma di installazione per identificare l'utente di un prodotto.
ms.assetid: da615cb4-d36d-4180-8f97-c9f83c0df1c6
title: Azione RegisterUser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f89d43d18839e806939b7a084d37840b9895fdc81efb79fc03867eebe4c5c57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626716"
---
# <a name="registeruser-action"></a>Azione RegisterUser

L'azione RegisterUser registra le informazioni utente con il programma di installazione per identificare l'utente di un prodotto.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

Non sono presenti restrizioni di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione   |
|-------|------------------------------|
| \[1\] | Informazioni utente registrate. |



 

## <a name="remarks"></a>Commenti

L'azione RegisterUser non viene eseguita durante un'installazione amministrativa. Se l'identificatore di prodotto immesso dall'utente non è stato convalidato dall'azione [ValidateProductID](validateproductid-action.md), la [**proprietà ProductID**](productid.md) non viene impostata e questa azione non esegue alcuna operazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Nome utente**](username.md)
</dt> <dt>

[**Companyname**](companyname.md)
</dt> <dt>

[**Productid**](productid.md)
</dt> </dl>

 

 



