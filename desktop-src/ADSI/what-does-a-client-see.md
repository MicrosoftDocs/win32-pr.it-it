---
title: Che cosa Visualizza un client
description: In questo argomento vengono elencati i modi in cui un client Visualizza i dati ADSI.
ms.assetid: 238eeea9-1303-4d37-bf09-ad03f1790c1b
ms.tgt_platform: multiple
keywords:
- estensioni ADSI, che cosa Visualizza un client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398c9fd2d603c1eebb18280c435bec7cb7cd8e14
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104517109"
---
# <a name="what-does-a-client-see"></a>Che cosa Visualizza un client?

-   Un client visualizza ADSI e tutti i relativi oggetti di estensione come un unico oggetto.
-   Un client ADSI rileva un'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che gestisce tutte le interfacce dual e dispatch nell'oggetto, indipendentemente dal fatto che l'interfaccia duale o dispatch venga implementata da Aggregator nel provider o da un'estensione. Vedere [risoluzione dei conflitti di nomi di funzione/proprietà in automazione nelle estensioni](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).
-   ADSI non espone informazioni sui tipi tramite i metodi [**IDispatch:: GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) o [**IDispatch:: GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) . ADSI fornisce informazioni sul tipo tramite la libreria dei tipi.

 

 