---
title: Registrazione del provider di servizi
description: Registrazione del provider di servizi
ms.assetid: 556d6519-bc24-446b-a360-e3d83b40d541
keywords:
- Windows Gestione dispositivi multimediali, registrazione dei provider di servizi
- Gestione dispositivi, registrazione dei provider di servizi
- guida per programmatori, registrazione di provider di servizi
- provider di servizi, registrazione di provider di servizi
- creazione di provider di servizi, registrazione di provider di servizi
- registrazione di provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f480fff04d34cf671bdc37e3bcded92c73f20d31d2fb67e4d6e41593a724d392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584287"
---
# <a name="registering-the-service-provider"></a>Registrazione del provider di servizi

Oltre a essere registrato come oggetto COM, un provider di servizi deve essere registrato come plug-in per Windows Gestione dispositivi multimediali. Per eseguire la registrazione, un provider di servizi deve creare la chiave del Registro di sistema seguente:

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Media Device Manager\Plugins\SP\<             `

In questa chiave, < *nome del provider* di > è il nome della DLL. Ad esempio, il provider di servizi di esempio usa MsHDSP. La chiave ProgID deve avere un valore stringa corrispondente al CLSID del provider di servizi. Ad esempio, il provider di servizi di esempio ha il valore "MDServiceProviderHD.MDServiceProviderHD".

L'implementazione di DLLRegisterServer del provider di servizi di esempio in Mdsp.cpp aggiunge questa chiave del Registro di sistema quando si registra la DLL del provider di servizi di esempio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un provider di servizi**](creating-a-service-provider.md)
</dt> </dl>

 

 




