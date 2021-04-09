---
title: Registrazione del provider di servizi
description: Registrazione del provider di servizi
ms.assetid: 556d6519-bc24-446b-a360-e3d83b40d541
keywords:
- Windows Media Gestione dispositivi, registrazione dei provider di servizi
- Gestione dispositivi, registrazione di provider di servizi
- Guida per programmatori, registrazione di provider di servizi
- provider di servizi, registrazione di provider di servizi
- creazione di provider di servizi, registrazione di provider di servizi
- registrazione di provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1226b724b06990fc1e000a522e3a61672789cf3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044252"
---
# <a name="registering-the-service-provider"></a>Registrazione del provider di servizi

Oltre a essere registrato come oggetto COM, un provider di servizi deve essere registrato come plug-in a Windows Media Gestione dispositivi. Per eseguire la registrazione, un provider di servizi deve creare la seguente chiave del registro di sistema:

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Media Device Manager\Plugins\SP\<             `

In questa chiave < *il nome del provider di servizi* > è il nome della dll. ad esempio, il provider di servizi di esempio utilizza MsHDSP. La chiave ProgID deve avere un valore stringa corrispondente al CLSID del provider di servizi. Ad esempio, il provider di servizi di esempio ha il valore "MDServiceProviderHD. MDServiceProviderHD".

L'implementazione del provider di servizi di esempio di DLLRegisterServer in MDSP. cpp aggiunge questa chiave del registro di sistema quando si registra la DLL del provider di servizi di esempio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un provider di servizi**](creating-a-service-provider.md)
</dt> </dl>

 

 




