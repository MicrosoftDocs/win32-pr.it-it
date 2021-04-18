---
description: Esistono due metodi mediante i quali un'applicazione host può cercare gli assembly affiancati.
ms.assetid: f34f8f39-f03c-4adf-afa8-9cb9ed48d149
title: Ricerca di assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f257b7da8099508fb268623a175d8ebd8e9d8337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317094"
---
# <a name="searching-for-assemblies"></a>Ricerca di assembly

Esistono due metodi mediante i quali un'applicazione host può cercare gli assembly affiancati.

I moduli ospitati possono registrarsi con l'applicazione host estendendo alcune informazioni di configurazione condivise. L'applicazione può quindi utilizzare queste informazioni di configurazione per caricare gli assembly necessari per la nuova funzionalità. Questa operazione può essere eseguita chiamando [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) nei manifesti specificati nei dati di registrazione, seguito dalla chiamata a [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per accedere al nuovo modulo. Si noti che con questo metodo, i nuovi componenti devono aggiornare lo stato di un'applicazione condivisa per indicare la loro presenza.

L'applicazione host può cercare attivamente gli assembly all'avvio usando [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) e [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) per cercare le dll o i manifesti in un percorso specificato e quindi usare [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) per accedere alle informazioni. Questo metodo non richiede la registrazione del componente.

 

 
