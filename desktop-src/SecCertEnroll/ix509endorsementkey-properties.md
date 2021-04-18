---
description: L'interfaccia IX509EndorsementKey espone le proprietà seguenti.
ms.assetid: 9E93622B-56E9-4F2F-9EFA-4F63D45EDCB6
title: Proprietà di IX509EndorsementKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4bbdbc464803988f5b1100ac42fc0e3697fb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314165"
---
# <a name="ix509endorsementkey-properties"></a>Proprietà di IX509EndorsementKey

L'interfaccia [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) espone le proprietà seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Proprietà length**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_length)<br/>             | Lunghezza in bit della chiave di verifica dell'autenticità. È possibile accedere a questa proprietà solo dopo che è stato chiamato il metodo [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) .<br/>                                                                                                                                                                                            |
| [**Opened (proprietà)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_opened)<br/>             | Indica se il metodo [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) è stato chiamato correttamente.<br/>                                                                                                                                                                                                                                            |
| [**Proprietà ProviderName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername)<br/> | Nome del provider di crittografia. Il valore predefinito è il provider di crittografia della piattaforma Microsoft. È necessario impostare la proprietà [**providerName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) prima di chiamare il metodo [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) . Non è possibile modificare la proprietà **providerName** dopo aver chiamato il metodo **Open** .<br/> |



 

 

 




