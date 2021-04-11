---
title: File di libreria, file di intestazione e impostazioni del compilatore
description: File di libreria, file di intestazione e impostazioni del compilatore
ms.assetid: 7563bb3a-7bea-4e0c-8205-a16b276c8d1e
keywords:
- Windows Media Format SDK, file di libreria DRM
- Windows Media Format SDK, file di libreria
- Windows Media Format SDK, file di intestazione DRM
- Windows Media Format SDK, file di intestazione
- Windows Media Format SDK, impostazioni del compilatore DRM
- Windows Media Format SDK, impostazioni del compilatore
- Digital Rights Management (DRM), file di libreria
- DRM (Digital Rights Management), file di libreria
- Digital Rights Management (DRM), file di intestazione
- DRM (Digital Rights Management), file di intestazione
- Digital Rights Management (DRM), impostazioni del compilatore
- DRM (Digital Rights Management), impostazioni del compilatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b0b10ea03cc08d5b689b74f9c647f7d0138fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116856"
---
# <a name="library-files-header-files-and-compiler-settings"></a>File di libreria, file di intestazione e impostazioni del compilatore

I componenti di programmazione delle API estese del client Windows Media DRM sono definiti nel file di intestazione wmdrmsdk. h e sono implementati nelle librerie wmdrmsdk. lib e mfuuid. lib.

Per alcune delle funzionalità delle API estese del client Windows Media DRM è necessario ottenere una libreria protetta da Microsoft. Questa libreria, denominata libreria stub in questa documentazione, è specifica del destinatario e specifica il livello di sicurezza dell'applicazione per le applicazioni. La libreria stub sostituisce wmdrmsdk. lib; non è mai necessario collegarsi a entrambi.

**Nota** La libreria stub DRM è separata dalla libreria stub utilizzata dal resto di Windows Media Format SDK, ma è concessa in licenza con lo stesso metodo.

**Nota** La libreria stub DRM deve essere collegata all'applicazione dopo il file di libreria MSVCRT. lib per evitare errori del linker.

La libreria stub contiene un certificato incorporato che può essere revocato da Microsoft se non si rispettano i termini e le condizioni del contratto di licenza.

I metodi specifici che richiedono la libreria stub sono contrassegnati nella documentazione. Se si tenta di usare un metodo di questo tipo senza collegarsi alla libreria stub, verrà restituito un \_ errore STUBLIB di NS E \_ DRM \_ \_ .

Non è possibile usare il sottosistema DRM in una compilazione di debug. Se si tenta di eseguire questa operazione, i metodi dell'API restituiranno l'errore di debug di NS \_ E \_ DRM \_ \_ non \_ consentito.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Per iniziare**](drm-getting-started.md)
</dt> <dt>

[**File di libreria e impostazioni del compilatore**](library-files-and-compiler-settings.md)
</dt> <dt>

[**Ottenere la libreria DRM necessaria**](obtaining-the-required-drm-library.md)
</dt> </dl>

 

 




