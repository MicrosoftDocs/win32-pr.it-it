---
title: Run-Time collegamento a Wtsapi32.dll
description: L'applicazione può usare l'API Servizi Desktop remoto per collegarsi dinamicamente alla Wtsapi32.dll in fase di esecuzione. A tale scopo, l'applicazione deve chiamare la funzione LoadLibrary per caricare Wtsapi32.dll.
ms.assetid: b8227e65-be08-4045-a74e-dd3f398a7b9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc686f26029ee9bfa4332215e27a587a7e57b78de9bd0d1043ee58541ef76194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127496"
---
# <a name="run-time-linking-to-wtsapi32dll"></a>Run-Time collegamento a Wtsapi32.dll

Se l'applicazione viene eseguita in un ambiente che non è un ambiente Servizi Desktop remoto, ma si vuole che l'applicazione fornirà funzionalità aggiuntive quando viene eseguita in un ambiente Servizi Desktop remoto, l'applicazione può usare l'API Servizi Desktop remoto per implementare le funzionalità aggiuntive e collegarsi dinamicamente al Wtsapi32.dll in fase di esecuzione. A tale scopo, l'applicazione deve chiamare la [**funzione LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) per caricare Wtsapi32.dll. Se la **chiamata a LoadLibrary** ha esito negativo, l'applicazione può essere eseguita usando le funzionalità di base. Se **LoadLibrary** ha esito positivo, l'applicazione può chiamare la [**funzione GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per recuperare i puntatori alle funzioni Servizi Desktop remoto da chiamare.

Se l'applicazione è destinata solo a un Servizi Desktop remoto, il collegamento dinamico non è necessario. In questo caso, è possibile includere Wtsapi32.h e collegarsi a Wtsapi32.lib. Quindi, se l'applicazione viene avviata in un ambiente diverso da Servizi Desktop remoto, verrà chiusa perché Wtsapi32.dll non è presente.

Per informazioni su come determinare se l'applicazione è in esecuzione in un ambiente Servizi Desktop remoto, vedere [Detecting the Servizi Desktop remoto Environment](detecting-the-terminal-services-environment.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida generali per la programmazione](general-programming-guidelines.md)
</dt> </dl>

 

 