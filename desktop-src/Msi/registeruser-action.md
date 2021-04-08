---
description: L'azione RegisterUser registra le informazioni utente con il programma di installazione per identificare l'utente di un prodotto.
ms.assetid: da615cb4-d36d-4180-8f97-c9f83c0df1c6
title: Azione RegisterUser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686628d29094f951994b072ad4451a383a405965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756464"
---
# <a name="registeruser-action"></a>Azione RegisterUser

L'azione RegisterUser registra le informazioni utente con il programma di installazione per identificare l'utente di un prodotto.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Non esistono restrizioni di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione   |
|-------|------------------------------|
| \[1\] | Informazioni utente registrate. |



 

## <a name="remarks"></a>Commenti

L'azione RegisterUser non viene eseguita durante un'installazione amministrativa. Se l'identificatore del prodotto immesso dall'utente non è stato convalidato dall' [azione ValidateProductID](validateproductid-action.md), la proprietà [**ProductID**](productid.md) non è impostata e questa azione non esegue alcuna operazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**NOME utente**](username.md)
</dt> <dt>

[**COMPANYNAME**](companyname.md)
</dt> <dt>

[**ProductID**](productid.md)
</dt> </dl>

 

 



