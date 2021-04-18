---
description: Acquisisci attributi del dispositivo
ms.assetid: dd24671a-0689-4490-8d18-2a33ed461e9d
title: Acquisisci attributi del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dd8dbcdf0a441ddb8a5ef2794526e961c22033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305510"
---
# <a name="capture-device-attributes"></a>Acquisisci attributi del dispositivo

Gli attributi seguenti sono correlati ai dispositivi di acquisizione:



| Attributo                                                                                                                     | Descrizione                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [\_ \_ \_ nome descrittivo dell'attributo MF DEVSOURCE \_](mf-devsource-attribute-friendly-name.md)                                          | Nome visualizzato del dispositivo.                                                          |
| [\_tipo di \_ supporto per attributi MF DEVSOURCE \_ \_](mf-devsource-attribute-media-type.md)                                                | Formato di output del dispositivo.                                                         |
| [\_tipo di \_ origine dell'attributo MF DEVSOURCE \_ \_](mf-devsource-attribute-source-type.md)                                              | Tipo di dispositivo, ad esempio acquisizione audio o acquisizione video.                         |
| [\_tipo di \_ origine attributo MF DEVSOURCE \_ \_ \_ AUDCAP \_ endpoint \_ ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md)     | ID endpoint per un dispositivo di acquisizione audio.                                        |
| [\_ \_ \_ \_ ruolo AUDCAP del tipo di origine dell' \_ attributo \_ MF DEVSOURCE](mf-devsource-attribute-source-type-audcap-role.md)                    | Ruolo del dispositivo per un dispositivo di acquisizione audio.                                        |
| [\_categoria di \_ origine attributo MF DEVSOURCE \_ \_ tipo \_ VidCap \_](mf-devsource-attribute-source-type-vidcap-category.md)            | Categoria del dispositivo per un dispositivo video.                                             |
| [\_tipo di origine dell'attributo MF DEVSOURCE \_ \_ \_ \_ VidCap \_ HW \_ source](mf-devsource-attribute-source-type-vidcap-hw-source.md)         | Specifica se un'origine di acquisizione video è un dispositivo hardware o software. |
| [\_tipo di \_ origine attributo MF DEVSOURCE \_ \_ \_ VidCap \_ Max \_ buffer](mf-devsource-attribute-source-type-vidcap-max-buffers.md)     | Specifica il numero massimo di frame che l'origine di acquisizione video registrerà nel buffer.   |
| [\_tipo di \_ origine attributo MF DEVSOURCE \_ \_ \_ VidCap \_ collegamento simbolico \_](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) | Collegamento simbolico per un driver di acquisizione video.                                       |
| [\_Timestamp HW \_ MFT \_ con \_ \_ attributo QPC](mft-hw-timestamp-with-qpc-attribute.md)                                           | Specifica se l'origine del dispositivo usa l'ora di sistema per gli indicatori di data e ora.           |



 

Questi attributi vengono usati con le funzioni seguenti:

-   [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



