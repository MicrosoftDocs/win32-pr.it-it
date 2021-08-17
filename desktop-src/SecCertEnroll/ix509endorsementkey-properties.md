---
description: L'interfaccia IX509EndorsementKey espone le proprietà seguenti.
ms.assetid: 9E93622B-56E9-4F2F-9EFA-4F63D45EDCB6
title: Proprietà IX509EndorsementKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41d135205680e4c998c1157844cfa66a9ef9bd7ef4df5ff8258a31e562a685e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117776189"
---
# <a name="ix509endorsementkey-properties"></a>Proprietà IX509EndorsementKey

[**L'interfaccia IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) espone le proprietà seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Proprietà Length**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_length)<br/>             | Lunghezza in bit della chiave di approvazione. È possibile accedere a questa proprietà solo dopo la [**chiamata al**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) metodo Open.<br/>                                                                                                                                                                                            |
| [**Proprietà Opened**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_opened)<br/>             | Indica se il [**metodo Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) è stato chiamato correttamente.<br/>                                                                                                                                                                                                                                            |
| [**ProviderName - proprietà**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername)<br/> | Nome del provider di crittografia. Il valore predefinito è Microsoft Platform Crypto Provider. È necessario impostare la [**proprietà ProviderName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) prima di chiamare il [**metodo Open.**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) Non è possibile modificare **la proprietà ProviderName** dopo aver chiamato il **metodo Open.**<br/> |



 

 

 




