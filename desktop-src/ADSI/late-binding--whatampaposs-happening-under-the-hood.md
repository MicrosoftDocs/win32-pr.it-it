---
title: Associazione tardiva di ciò che accade sotto il cofano
description: Questo argomento descrive il funzionamento dell'associazione tardiva in ADSI.
ms.assetid: f4ff19fc-d69e-4528-a6e2-2544d9149e8c
ms.tgt_platform: multiple
keywords:
- estensioni ADSI, associazione tardiva, cosa accade sotto il cofano
- associazione ad Active Directory, associazione tardiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c479472a2974f31e8ecdd4308b01cf7c7251eada3f907d5d90ecf152028399b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637891"
---
# <a name="late-binding-whats-happening-under-the-hood"></a>Associazione tardiva: cosa accade sotto il cofano?

L'elenco seguente illustra il processo generale per l'esecuzione di un'associazione tardiva:

-   Un elemento viene associato a un oggetto directory ADSI. Ad esempio, "LDAP://CN=Jeffsmith,OU=Sales,DC=Fabrikam,DC=COM" esegue il binding usando l'associazione tardiva COM. In questo modo ADSI chiama il [**metodo QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) sull'interfaccia **IDispatch.**
-   ADSI trova un oggetto nella classe utente e crea un oggetto che supporta le interfacce appropriate, ad esempio [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).
-   ADSI esegue una ricerca nel Registro di sistema e trova i CLSID di estensione per l'utente. Tenere presente che ADSI memorizza nella cache questi dati.
-   Viene chiamata una chiamata al **metodo MyNewMethod.** ADSI cerca l'ID dispatch e gli ID dispatch per altre estensioni ADSI. ADSI trova quindi l'estensione che serve questa chiamata e chiama [**l'interfaccia IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) per tale estensione.
-   L'estensione esegue la funzione .
-   A questo punto, il writer client richiama il **metodo YourNewMethod** usando [**l'interfaccia IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) per l'estensione corrente. L'implementazione **IDispatch dell'estensione** delega di nuovo a **IDispatch** per ADSI.
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) per ADSI cerca nuovamente l'estensione appropriata o se stessa, quindi chiama l'estensione appropriata usando [**l'interfaccia IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) per tale estensione.

 

 