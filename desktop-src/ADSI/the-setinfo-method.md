---
title: Metodo seinfo
description: Il metodo IADs SetInfo Salva i valori correnti per le proprietà di questo oggetto Active Directory dalla cache delle proprietà nell'archivio directory sottostante. Questo è analogo allo scaricamento di un buffer su disco.
ms.assetid: e4152b3d-3a59-4f69-9765-03cdf6286459
ms.tgt_platform: multiple
keywords:
- SetInfo ADSI, uso
- Proprietà ADSI, salvare i valori correnti per le proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5965a46e5accd2a00adc006fe37511de13ff0df3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328348"
---
# <a name="the-setinfo-method"></a>Metodo seinfo

Il metodo [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) Salva i valori correnti per le proprietà di questo oggetto Active Directory dalla cache delle proprietà nell'archivio directory sottostante. Questo è analogo allo scaricamento di un buffer su disco.

Per aggiornare gli oggetti già presenti nella directory, è necessario creare una nuova voce di directory [**per gli oggetti**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) appena creati.

Al momento della chiamata a [**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) , se i valori della cache delle proprietà sono stati scritti con un codice di controllo [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) , ad esempio \_ l'aggiornamento delle proprietà Ads \_ o \_ la proprietà Ads \_ Clear, le richieste appropriate vengono passate al servizio directory sottostante.

 

 




