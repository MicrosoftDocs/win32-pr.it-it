---
title: Run-Time il collegamento a Wtsapi32.dll
description: L'applicazione può usare l'API Servizi Desktop remoto per collegare in modo dinamico al Wtsapi32.dll in fase di esecuzione. A tale scopo, l'applicazione deve chiamare la funzione LoadLibrary per caricare Wtsapi32.dll.
ms.assetid: b8227e65-be08-4045-a74e-dd3f398a7b9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c53a992955876bf812a87168d2c74b776cf0d4e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399418"
---
# <a name="run-time-linking-to-wtsapi32dll"></a>Run-Time il collegamento a Wtsapi32.dll

Se l'applicazione viene eseguita in un ambiente che non è un ambiente Servizi Desktop remoto, ma si vuole che l'applicazione fornisca funzionalità aggiuntive quando viene eseguita in un ambiente Servizi Desktop remoto, l'applicazione può usare l'API Servizi Desktop remoto per implementare la funzionalità aggiuntiva e collegarsi dinamicamente al Wtsapi32.dll in fase di esecuzione. A tale scopo, l'applicazione deve chiamare la funzione [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) per caricare Wtsapi32.dll. Se la chiamata a **LoadLibrary** ha esito negativo, l'applicazione può essere eseguita usando le funzionalità di base. Se **LoadLibrary** ha esito positivo, l'applicazione può chiamare la funzione [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per recuperare i puntatori alle funzioni Servizi Desktop remoto che si desidera chiamare.

Se l'applicazione è destinata solo a un ambiente Servizi Desktop remoto, il collegamento dinamico non è necessario. In questo caso, è possibile includere wtsapi32. h e il collegamento a wtsapi32. lib. Quindi, se l'applicazione viene avviata in un ambiente diverso da Servizi Desktop remoto, verrà chiusa perché Wtsapi32.dll non è presente.

Per informazioni su come determinare se l'applicazione è in esecuzione in un ambiente di Servizi Desktop remoto, vedere [rilevamento dell'ambiente Servizi Desktop remoto](detecting-the-terminal-services-environment.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida generali per la programmazione](general-programming-guidelines.md)
</dt> </dl>

 

 