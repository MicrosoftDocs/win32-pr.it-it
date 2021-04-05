---
description: È possibile scrivere moduli criteri nel linguaggio di programmazione C, C++ o Visual Basic.
ms.assetid: 37a93c67-02f2-4c4e-a000-2bb98e0ca948
title: Scrittura di moduli personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92247cd6b975bac520032dcc3aada1328f7b6c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967617"
---
# <a name="writing-custom-modules"></a>Scrittura di moduli personalizzati

È possibile scrivere moduli criteri nel linguaggio di programmazione C, C++ o Visual Basic. Il compilatore Microsoft richiesto è disponibile in Visual C++ versione 5,0 o successiva o in Visual Basic versione 5,0 o successiva. Un' [*autorità di certificazione*](../secgloss/c-gly.md) (CA) dell'organizzazione (Enterprise) deve usare solo il modulo criteri di organizzazione fornito da Microsoft.

Quando si scrive un modulo criteri personalizzato, è necessario implementare [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) . Inoltre, è necessario implementare [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) quando si scrive un modulo criteri personalizzato.

I moduli criteri possono chiamare i metodi di [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) per facilitare l'elaborazione di una [*richiesta di certificato*](../secgloss/c-gly.md). **ICertServerPolicy** consente di impostare e recuperare le proprietà e le estensioni del certificato.

Per ulteriori informazioni, vedere gli argomenti seguenti.



| Argomento                                                                      | Descrizione                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [Impostazione delle proprietà del certificato](setting-certificate-properties.md)       | Impostazione delle proprietà di un certificato |
| [Scrittura di moduli di uscita personalizzati](writing-custom-exit-modules.md)             | Scrittura di moduli di uscita personalizzati             |
| [Scrittura di gestori estensioni personalizzati](writing-custom-extension-handlers.md) | Scrittura di gestori estensioni personalizzati       |



 

 

 
