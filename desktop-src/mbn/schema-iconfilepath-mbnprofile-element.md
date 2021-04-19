---
description: Contiene il percorso del file icona per la connessione.
ms.assetid: 9daf4916-914b-4326-9933-b433cc00b4c1
title: Elemento ICONFilePath (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICONFilePath
api_type:
- Schema
ms.openlocfilehash: 6b1e98f76fe2f83ce214076223b5a1439bd0ea45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307539"
---
# <a name="iconfilepath-mbnprofile-element"></a>Elemento ICONFilePath (MBNProfile)

L'elemento **ICONFilePath (MBNProfile)** contiene il percorso del file icona per la connessione.

L'interfaccia utente di connessione al sistema operativo visualizzerà questa icona quando si effettua una connessione utilizzando questo elemento.

Quando si passa il codice XML per la creazione del profilo nel metodo [**CreateConnectionProfile**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) dell'interfaccia [**IMbnConnectionProfileManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) , questo percorso deve puntare al percorso di origine del file icona. Al completamento della creazione dell'oggetto [**IMbnConnectionProfile**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) , il servizio Mobile Broadband copia il file dell'icona nell'archivio interno e il percorso del profilo verrà modificato in modo da riflettere questo problema.

Il file icona deve essere in formato BMP con la dimensione 32X32 pixel.

Questo elemento è una stringa di lunghezza massima di 1024 caratteri, che contiene un percorso di file assoluto.

L'elemento è facoltativo.

``` syntax
<xs:element name="ICONFilePath"
    type="iconFileType"
 />
```

L'elemento **ICONFilePath** è definito dall'elemento [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




