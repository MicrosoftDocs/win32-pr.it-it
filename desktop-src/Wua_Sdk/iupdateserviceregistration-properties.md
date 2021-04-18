---
description: L'interfaccia IUpdateServiceRegistration definisce le proprietà seguenti.
ms.assetid: 2bcde8b4-7bff-4887-8080-89da817afb5f
title: Proprietà di IUpdateServiceRegistration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716c06f2fc8ed9a7ce12542a09440cf0ec0b5c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305838"
---
# <a name="iupdateserviceregistration-properties"></a>Proprietà di IUpdateServiceRegistration

L'interfaccia **IUpdateServiceRegistration** definisce le proprietà seguenti.



| Proprietà                                                                                      | Descrizione                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsPendingRegistrationWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_ispendingregistrationwithau) | Ottiene un valore booleano che indica se il servizio verrà registrato anche con Aggiornamenti automatici, quando viene aggiunto.                                  |
| [**RegistrationState**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_registrationstate)                     | Ottiene un valore [**UpdateServiceRegistrationState**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) che indica lo stato corrente della registrazione del servizio. |
| [**Servizio**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_service)                                         | Ottiene un puntatore a un'interfaccia [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) . Questa proprietà è la proprietà predefinita.                                    |



 

 

 



