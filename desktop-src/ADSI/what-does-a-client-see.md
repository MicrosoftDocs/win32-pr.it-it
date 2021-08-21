---
title: Cosa visualizza un client
description: In questo argomento vengono elencati i modi in cui un client visualizza i dati ADSI.
ms.assetid: 238eeea9-1303-4d37-bf09-ad03f1790c1b
ms.tgt_platform: multiple
keywords:
- estensioni ADSI, cosa visualizza un client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d38563de47cfc80bdcf265249bf3e4cf10bc46471e18672221fed8c3047efa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082175"
---
# <a name="what-does-a-client-see"></a>Cosa visualizza un client?

-   Un client vede ADSI e tutti i relativi oggetti di estensione come un unico oggetto.
-   Un client ADSI vede [**un'interfaccia IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che gestisce tutte le interfacce duali e dispatch nell'oggetto, indipendentemente dal fatto che l'interfaccia duale o dispatch sia implementata dall'aggregatore nel provider o da un'estensione. Vedere [Risoluzione dei conflitti dei nomi di funzione/proprietà nell'automazione nelle estensioni.](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md)
-   ADSI non espone informazioni sul tipo tramite i [**metodi IDispatch::GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) [**o IDispatch::GetTypeInfoCount.**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) ADSI fornisce informazioni sui tipi tramite la libreria dei tipi.

 

 