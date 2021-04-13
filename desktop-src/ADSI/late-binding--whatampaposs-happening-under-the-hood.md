---
title: Associazione tardiva di ciò che accade dietro le quinte
description: In questo argomento viene descritto il funzionamento dell'associazione tardiva in ADSI.
ms.assetid: f4ff19fc-d69e-4528-a6e2-2544d9149e8c
ms.tgt_platform: multiple
keywords:
- estensioni ADSI, associazione tardiva, cosa accade dietro le quinte
- Binding AD, associazione tardiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299b715325e4eda88a0eeaca2b22b4bdaa15a96
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474227"
---
# <a name="late-binding-whats-happening-under-the-hood"></a>Associazione tardiva: cosa succede dietro le quinte?

Nell'elenco seguente viene descritto il processo generale per l'esecuzione di un'associazione tardiva:

-   Un elemento viene associato a un oggetto directory ADSI. Ad esempio, "LDAP://CN = SergioMelchiori, OU = Sales, DC = Fabrikam, DC = COM" viene associato utilizzando l'associazione COM tardiva. In questo modo ADSI chiama il metodo [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) sull'interfaccia **IDispatch** .
-   ADSI trova un oggetto nella classe utente e crea un oggetto che supporta le interfacce appropriate, ad esempio [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).
-   ADSI esegue una ricerca nel registro di sistema e trova i CLSID di estensione per l'utente. Tenere presente che ADSI memorizza nella cache i dati.
-   Un elemento effettua una chiamata al metodo **MyNewMethod** . ADSI cerca l'ID dispatch e gli ID dispatch per altre estensioni ADSI. ADSI trova quindi l'estensione che serve questa chiamata e chiama l'interfaccia [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) per tale estensione.
-   L'estensione esegue la funzione.
-   A questo punto, il writer client richiama il metodo **YourNewMethod** usando l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) per l'estensione corrente. L'implementazione **IDispatch** dell'estensione delega di nuovo **IDispatch** per ADSI.
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) per ADSI cerca di nuovo l'estensione appropriata, o se stesso, chiama l'estensione appropriata usando l'interfaccia [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) per tale estensione.

 

 