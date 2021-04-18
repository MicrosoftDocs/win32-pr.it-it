---
description: In ognuna delle sezioni seguenti viene illustrata una funzione esportata da Xenroll.dll per gestire i messaggi PFX (Personal Information Exchange).
ms.assetid: f7e6b3a6-eae4-49f8-a624-609742741560
title: Funzioni scambio informazioni personali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea1670e6017cd30ed8358d2670585727667068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315396"
---
# <a name="personal-information-exchange-functions"></a>Funzioni scambio informazioni personali

In ognuna delle sezioni seguenti viene illustrata una funzione esportata da Xenroll.dll per gestire i messaggi PFX (Personal Information Exchange). In ogni sezione viene inoltre illustrato come utilizzare CertEnroll.dll per sostituire la funzione o indicare che non esiste alcun mapping tra le due librerie.

## <a name="createfilepfxwstr"></a>createFilePFXWStr

La funzione [**createFilePFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) in Xenroll.dll salva una catena di certificati e una [*chiave privata*](/windows/desktop/SecGloss/p-gly) in un file usando il formato pfx.

La libreria CertEnroll.dll non implementa direttamente le funzionalità per copiare il messaggio PFX in un file. È tuttavia possibile utilizzare il metodo [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) sull'interfaccia [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) per creare un messaggio PFX codificato e scrivere una funzione personalizzata per salvare il messaggio in un file.

## <a name="createpfxwstr"></a>createPFXWStr

La funzione [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) in Xenroll.dll salva una catena di certificati e una chiave privata in una stringa di formato pfx.

È possibile usare il metodo [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) sull'interfaccia [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) per creare un messaggio PFX codificato che contiene la catena di certificati e la chiave. È possibile specificare una password, le opzioni di esportazione e il tipo di codifica. Per recuperare una stringa equivalente a quella restituita da [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr), passare il flag XCN \_ crypt \_ String \_ Binary nell'oggetto nel parametro *Encoding* del metodo [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping Xenroll.dll CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**Metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
