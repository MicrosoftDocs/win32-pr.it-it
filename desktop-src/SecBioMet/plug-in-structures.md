---
title: Strutture di plug-in
description: Strutture per lo sviluppo di applicazioni client da parte dell'API Windows Biometric Framework.
ms.assetid: 64fb908c-72c2-4639-a2f6-77ede080512c
keywords:
- API Windows Biometric Framework API di Windows Biometric Framework, strutture di plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193b5a99f30c76e8e6e2ab7ebf0242cf56905816
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331671"
---
# <a name="plug-in-structures"></a>Strutture di plug-in

Le strutture seguenti sono supportate per lo sviluppo di applicazioni client da parte dell'API Windows Biometric Framework.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                | Descrizione                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_criteri dell'account WINBIO \_**](winbio-account-policy.md)<br/>                                  | Contiene criteri di antispoofing predefiniti o specifici dell'account.<br/>                                                         |
| [**\_versione dell' \_ interfaccia dell'adattatore WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_adapter_interface_version)<br/>           | Contiene un numero di versione principale e secondario utilizzato nelle tabelle di interfaccia del motore, del sensore e dell'adattatore di archiviazione.<br/>                |
| [**\_interfaccia del motore WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_engine_interface)<br/>                              | Contiene i puntatori alle funzioni dell'adattatore del motore personalizzato.<br/>                                                                 |
| [**WINBIO \_ parametri di registrazione estesi \_ \_**](winbio-extended-enrollment-parameters.md)<br/> | Contiene informazioni aggiuntive necessarie per la creazione di un modello di registrazione da un adattatore del motore. <br/>                            |
| [**\_pipeline WINBIO**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_pipeline)<br/>                                               | Contiene informazioni di contesto condivise utilizzate dal sensore, dal motore e dai componenti dell'adattatore di archiviazione in un'unica unità biometrica.<br/> |
| [**\_interfaccia del sensore WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface)<br/>                              | Contiene i puntatori alle funzioni dell'adattatore del sensore personalizzato.<br/>                                                                 |
| [**\_interfaccia di archiviazione WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface)<br/>                            | Contiene i puntatori alle funzioni dell'adattatore di archiviazione personalizzato.<br/>                                                                |
| [**\_record di archiviazione WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_record)<br/>                                  | Contiene un modello biometrico e i dati associati in un formato standard.<br/>                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al plug-in](plug-in-reference.md)
</dt> <dt>

[Funzioni plug-in](plug-in-functions.md)
</dt> <dt>

[**WbioQueryEngineInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioqueryengineinterface)
</dt> <dt>

[**WbioQuerySensorInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)
</dt> <dt>

[**WbioQueryStorageInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)
</dt> </dl>

 

 





