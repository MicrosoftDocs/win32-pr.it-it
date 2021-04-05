---
description: Ogni proprietà del controllo di registrazione certificati è di lettura/scrittura e presenta un valore predefinito inizializzato nonché un set di valori accettabili.
ms.assetid: e31dd6df-bc2a-401f-9343-a7dbb0f374bb
title: Uso delle proprietà del controllo di registrazione certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192ad4efd3d2438f800d4a3872a8cf1057ca9920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753434"
---
# <a name="using-the-certificate-enrollment-control-properties"></a>Uso delle proprietà del controllo di registrazione certificati

Ogni proprietà del controllo di registrazione certificati è di lettura/scrittura e presenta un valore predefinito inizializzato nonché un set di valori accettabili. È possibile impostare una proprietà su qualsiasi valore all'interno di questo set per modificare il comportamento dei metodi che utilizzano la proprietà. Per ottenere un comportamento desiderato, impostare la proprietà prima di chiamare il metodo che usa il valore della proprietà.

Si noti, tuttavia, che dopo la chiamata dei metodi seguenti

-   [**acceptPKCS7**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptpkcs7)
-   [**acceptFilePKCS7**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptfilepkcs7)
-   [**createPKCS10**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createpkcs10)
-   [**createFilePKCS10**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createfilepkcs10)

le proprietà seguenti sono bloccate dalla reimpostazione

-   [**ProviderType**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providertype)
-   [**KeySpec**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_keyspec)
-   [**ProviderFlags**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providerflags)
-   [**ContainerName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_containername)
-   [**ProviderName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providername)

a meno che non venga chiamato il metodo [**ICEnroll4:: Reset**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset) .

Per informazioni sui singoli metodi e proprietà, vedere gli argomenti di riferimento relativi a tali proprietà e metodi nel [riferimento alla crittografia](cryptography-reference.md).

Le sezioni seguenti contengono informazioni specifiche della lingua per l'impostazione e il recupero delle proprietà del controllo di registrazione certificati:

-   [Proprietà del controllo di registrazione certificati in C++](certificate-enrollment-control-properties-in-c-.md)

 

 
