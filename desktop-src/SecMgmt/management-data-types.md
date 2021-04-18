---
description: Elenca i tipi di dati utilizzati dalle DLL allegati alla configurazione di sicurezza e dalle relative funzioni di supporto.
ms.assetid: 1d3bdf0d-320c-4b25-9e9b-fda134876979
title: Tipi di dati di gestione della sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae7efedb32ab545b903c61819042e32b7d83dbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312767"
---
# <a name="security-management-data-types"></a>Tipi di dati di gestione della sicurezza

I tipi di dati di gestione della sicurezza includono i seguenti:

-   [Tipi di dati allegati](#attachment-data-types)
-   [Tipi di dati dei criteri LSA](#lsa-policy-data-types)

## <a name="attachment-data-types"></a>Tipi di dati allegati

I tipi di dati seguenti vengono utilizzati dalle DLL degli allegati di configurazione di sicurezza e dalle relative funzioni di supporto.



| Tipo di dati                                                    | Descrizione                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_contesto di enumerazione SCE \_**](sce-enumeration-context.md) | Usato dalla funzione [**\_ \_ informazioni query PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) per spostarsi nel database di sicurezza.                                                                                                                                              |
| [**\_handle SCE**](sce-handle.md)                            | Usato dalle informazioni sulla [**\_ query PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) e da [**PFSCE \_ set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) per passare le informazioni tra l'allegato e il database di sicurezza.                                                                                 |
| [**SCESTATUS**](scestatus.md)                               | Il tipo di dati viene usato dall'API del set di strumenti di configurazione della sicurezza per restituire informazioni sui risultati di una chiamata di funzione.                                                                                                                                    |
| [**\_handle SCESVC**](scesvc-handle.md)                      | Utilizzato dai metodi delle interfacce [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) e [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) per passare informazioni tra lo snap-in configurazione di sicurezza e l'estensione dello snap-in. |
| [**\_tipo di informazioni SCESVC \_**](/windows/desktop/api/Scesvc/ne-scesvc-scesvc_info_type)               | L'enumerazione viene utilizzata [**dalle \_ \_ informazioni di query PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) e [**PFSCE \_ set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) per indicare il tipo di informazioni richieste da o passate al database di sicurezza.                                                 |



 

## <a name="lsa-policy-data-types"></a>Tipi di dati dei criteri LSA

I tipi di dati seguenti vengono utilizzati dalle funzioni di gestione dei criteri LSA.



| Tipo di dati                                                  | Descrizione                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------|
| [**\_handle di enumerazione LSA \_**](lsa-enumeration-handle.md) | Utilizzato per tenere traccia delle enumerazioni in cui sono richieste più chiamate di funzione. |
| [**\_handle LSA**](lsa-handle.md)                          | Handle per un oggetto [**criteri**](policy-object.md) .                       |



 

 

 
