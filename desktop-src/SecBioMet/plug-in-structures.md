---
title: Strutture dei plug-in
description: Strutture per lo sviluppo di applicazioni client da parte dell Windows API Biometric Framework.
ms.assetid: 64fb908c-72c2-4639-a2f6-77ede080512c
keywords:
- Windows API Biometric Framework Windows API Biometric Framework , strutture plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e150dd043a8c95e91d0f9095e23584544f43a503a709ae54c9180e06aa40bdaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101241"
---
# <a name="plug-in-structures"></a>Strutture dei plug-in

Le strutture seguenti sono supportate per lo sviluppo di applicazioni client dall'API Windows Biometric Framework.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                | Descrizione                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**CRITERI DELL'ACCOUNT WINBIO \_ \_**](winbio-account-policy.md)<br/>                                  | Contiene un criterio antispoofing predefinito o specifico dell'account.<br/>                                                         |
| [**VERSIONE DELL'INTERFACCIA \_ \_ DELL'ADAPTER WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_adapter_interface_version)<br/>           | Contiene un numero di versione principale e secondario usato nelle tabelle di interfaccia del motore, del sensore e dell'adattatore di archiviazione.<br/>                |
| [**INTERFACCIA DEL MOTORE WINBIO \_ \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_engine_interface)<br/>                              | Contiene puntatori alle funzioni dell'adattatore del motore personalizzato.<br/>                                                                 |
| [**PARAMETRI DI REGISTRAZIONE \_ ESTESA WINBIO \_ \_**](winbio-extended-enrollment-parameters.md)<br/> | Contiene informazioni aggiuntive necessarie a un adattatore motore per creare un modello di registrazione. <br/>                            |
| [**WINBIO \_ PIPELINE**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_pipeline)<br/>                                               | Contiene informazioni di contesto condiviso usate dai componenti sensore, motore e adattatore di archiviazione in una singola unità biometrica.<br/> |
| [**INTERFACCIA DEL SENSORE WINBIO \_ \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface)<br/>                              | Contiene puntatori alle funzioni dell'adattatore del sensore personalizzato.<br/>                                                                 |
| [**INTERFACCIA DI ARCHIVIAZIONE \_ WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface)<br/>                            | Contiene puntatori alle funzioni dell'adattatore di archiviazione personalizzato.<br/>                                                                |
| [**RECORD DI ARCHIVIAZIONE WINBIO \_ \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_record)<br/>                                  | Contiene un modello biometrico e i dati associati in un formato standard.<br/>                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sul plug-in](plug-in-reference.md)
</dt> <dt>

[Funzioni plug-in](plug-in-functions.md)
</dt> <dt>

[**WbioQueryEngineInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioqueryengineinterface)
</dt> <dt>

[**WbioQuerySensorInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)
</dt> <dt>

[**WbioQueryStorageInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)
</dt> </dl>

 

 





