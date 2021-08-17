---
description: Ognuna delle sezioni seguenti illustra una funzione esportata da Xenroll.dll gestire i messaggi PFX (Personal Information Exchange).
ms.assetid: f7e6b3a6-eae4-49f8-a624-609742741560
title: Funzioni di gestione delle Exchange personali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1e7cddcda00131b64c5fe6122d777695bbab4f80cbac8e71648a2197fed036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774684"
---
# <a name="personal-information-exchange-functions"></a>Funzioni di gestione delle Exchange personali

Ognuna delle sezioni seguenti illustra una funzione esportata da Xenroll.dll gestire i messaggi PFX (Personal Information Exchange). Ogni sezione illustra anche come usare CertEnroll.dll per sostituire la funzione o indica che non esiste alcun mapping tra le due librerie.

## <a name="createfilepfxwstr"></a>createFilePFXWStr

La [**funzione createFilePFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) in Xenroll.dll salva una catena di certificati e una chiave privata [*in*](/windows/desktop/SecGloss/p-gly) un file usando il formato PFX.

La CertEnroll.dll non implementa direttamente la funzionalità per copiare il messaggio PFX in un file. È tuttavia possibile usare il [**metodo CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) nell'interfaccia [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) per creare un messaggio PFX codificato e scrivere una funzione personalizzata per salvare il messaggio in un file.

## <a name="createpfxwstr"></a>createPFXWStr

La [**funzione createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) in Xenroll.dll salva una catena di certificati e una chiave privata in una stringa di formato PFX.

È possibile usare il [**metodo CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) nell'interfaccia [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) per creare un messaggio PFX codificato contenente la catena di certificati e la chiave. È possibile specificare una password, le opzioni di esportazione e il tipo di codifica. Per recuperare una stringa equivalente a quella restituita da [**createPFXWStr,**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr)passare il flag XCN CRYPT STRING BINARY nel parametro Encoding del \_ \_ metodo \_ [**CreatePFX.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**Registrazione IX509**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
