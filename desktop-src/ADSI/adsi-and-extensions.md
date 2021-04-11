---
title: Come ADSI integra le estensioni
description: Linee guida che descrivono il modo in cui ADSI interagisce con le estensioni.
ms.assetid: 00301551-ec56-4cb4-8e77-264c3ad48814
ms.tgt_platform: multiple
keywords:
- estensioni ADSI
- ADSI ed estensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956a76954851ea54b4eae99bfa45102a3b2fefa5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047357"
---
# <a name="how-adsi-integrates-extensions"></a>Come ADSI integra le estensioni

Le linee guida seguenti descrivono il modo in cui ADSI interagisce con le estensioni:

-   Un elemento viene associato a un oggetto directory ADSI. Ad esempio, "LDAP://CN = SergioMelchiori, OU = Sales, DC = Fabrikam, DC = COM".
-   ADSI indica che l'oggetto si trova nella classe **User** .
-   ADSI esegue una ricerca nel registro di sistema e identifica i CLSID di estensione per l' **utente**. Tenere presente che ADSI memorizza nella cache i dati.
-   Un elemento chiama il metodo **QueryInterface** per IID \_ IMyExtension. ADSI Cerca le interfacce associate all'oggetto **utente** , iniziando con le proprie interfacce, quindi esaminando le interfacce di estensione.
-   Se viene trovata una corrispondenza, ADSI crea un'istanza del componente che supporta IID \_ IMyExtension e chiama **QueryInterface** per l'estensione. Viene restituita l'interfaccia risultante.
-   L'utente usa questa interfaccia per chiamare i metodi di interfaccia.
-   Il client chiama quindi **QueryInterface** per IID \_ IYourExtension, che si trova in un componente diverso. Questo componente delega la chiamata **QueryInterface** all'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) di aggregator, che si verifica come ADSI.
-   Anche in questo caso, ADSI Cerca le interfacce e crea l'istanza del componente.

 

 