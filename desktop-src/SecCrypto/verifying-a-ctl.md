---
description: Per rendere più difficile per un intertruso sostituire un elenco di certificati attendibili (CTL, Certificate Trust List) fasullo per uno esistente, verificare la firma nel CTL ogni volta che viene usato il CTL.
ms.assetid: 24ba6955-f6d1-4123-ab39-50385f6e03a0
title: Verifica di un CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac88362c96d5b419a7c16731e31456b569079d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527613"
---
# <a name="verifying-a-ctl"></a>Verifica di un CTL

Per rendere più difficile per un intertruso sostituire un [*elenco di certificati attendibili (CTL, Certificate Trust List*](../secgloss/c-gly.md) ) fasullo per uno esistente, verificare la firma nel CTL ogni volta che viene usato il CTL. Non usare un elenco di scopi consentiti che non contenga una firma attendibile.

**Per verificare una firma CTL**

1.  Aprire l' [*archivio certificati*](../secgloss/c-gly.md) contenente l'elenco di scopi consentiti desiderato.
2.  Ottenere un handle per un [**\_ contesto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) per l'elenco di scopi consentiti. Questa operazione può essere eseguita chiamando le funzioni che restituiscono un handle al **\_ contesto CTL**, ad esempio [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).
3.  Chiamare [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), passando il [**\_ contesto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) recuperato nel passaggio 2 nel parametro *hCryptMsg* , un handle all'archivio certificati contenente il certificato dell'origine attendibile per scopi consentiti nel parametro *rghSignerStore* e il \_ flag del firmatario attendibile CMSG \_ \_ nel parametro *dwFlags* . Se la funzione restituisce **true**, la firma è stata verificata e viene restituito un puntatore al [**\_ contesto PCCERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del firmatario CTL nel parametro *ppSigner* .

 

 
