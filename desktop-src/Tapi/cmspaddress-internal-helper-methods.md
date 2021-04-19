---
description: Nell'elenco seguente sono inclusi i metodi di indirizzi di CMSP interni.
ms.assetid: 2016a776-1464-46b5-96b9-b045834f9e38
title: Metodi helper interni di CMSPAddress
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17064d161e2a073addb2e8eef6d9d290b41278b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319882"
---
# <a name="cmspaddress-internal-helper-methods"></a>Metodi helper interni di CMSPAddress



| Metodi helper interni di CMSPAddress                                        | Descrizione                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetStaticTerminals**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals)               | Chiamato da [**get \_ StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals) e [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals) per ottenere una matrice di terminali statici che possono essere usati in questo indirizzo.                                     |
| [**GetDynamicTerminalClasses**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses) | Chiamato da [**get \_ DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses) e [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) per ottenere una matrice di classi di terminali dinamici che possono essere utilizzate per questo indirizzo. |
| [**UpdateTerminalList**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-updateterminallist)               | Popola l'elenco di terminali statici del MSP.                                                                                                                                                                                                                                |
| [**ReceiveTSPAddressData**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-receivetspaddressdata)         | Chiamato quando un messaggio di dati di un TSP deve essere elaborato dall'indirizzo anziché da una chiamata specifica.                                                                                                                                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CMSPAddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 
