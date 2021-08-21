---
title: Metodo SetInfo
description: Il metodo IADs SetInfo salva i valori correnti per le proprietà di questo oggetto Active Directory dalla cache delle proprietà all'archivio directory sottostante. Ciò è analogo a quello dello scaricamento di un buffer su disco.
ms.assetid: e4152b3d-3a59-4f69-9765-03cdf6286459
ms.tgt_platform: multiple
keywords:
- SetInfo ADSI ,using
- properties ADSI, salvare i valori correnti per le proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e732cefa2d09b92f4fefec2b56f5f2ac8a99f77b2c7720822173cfaa647d7c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023139"
---
# <a name="the-setinfo-method"></a>Metodo SetInfo

Il [**metodo IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) salva i valori correnti per le proprietà per questo oggetto Active Directory dalla cache delle proprietà all'archivio directory sottostante. Ciò è analogo a quello dello scaricamento di un buffer su disco.

[**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) aggiorna gli oggetti già esistenti nella directory o crea una nuova voce di directory per gli oggetti appena creati.

Al momento della chiamata [**a SetInfo,**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) se i valori della cache delle proprietà sono stati scritti con un codice di controllo [**PutEx,**](/windows/desktop/api/Iads/nf-iads-iads-putex) ad esempio ADS PROPERTY UPDATE o \_ ADS PROPERTY CLEAR, le richieste appropriate vengono passate al servizio \_ \_ directory \_ sottostante.

 

 




