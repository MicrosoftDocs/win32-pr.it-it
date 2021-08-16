---
description: Contiene il percorso del file dell'icona per la connessione.
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
ms.openlocfilehash: ea662a7519a8705818ef502f5b797f437b0f89bee649d0bde18ce6f71b099d74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035819"
---
# <a name="iconfilepath-mbnprofile-element"></a>Elemento ICONFilePath (MBNProfile)

**L'elemento ICONFilePath (MBNProfile)** contiene il percorso del file dell'icona per la connessione.

L'interfaccia utente di connessione del sistema operativo visualizza questa icona quando viene stabilita una connessione usando questo elemento.

Quando si passa il codice XML per la creazione del profilo nel [**metodo CreateConnectionProfile**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) dell'interfaccia [**IMbnConnectionProfileManager,**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) questo percorso deve puntare al percorso di origine del file di icona. Al completamento della creazione dell'oggetto [**IMbnConnectionProfile,**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) il servizio Mobile Broadband copierà il file dell'icona nell'archivio interno e il percorso del profilo verrà modificato in base a questo.

Il file dell'icona deve .bmp formato con dimensioni di 32x32 pixel.

Questo elemento è una stringa di lunghezza massima di 1024 caratteri, contenente un percorso di file assoluto.

L'elemento è facoltativo.

``` syntax
<xs:element name="ICONFilePath"
    type="iconFileType"
 />
```

**L'elemento ICONFilePath** è definito dall'elemento [**MBNProfile.**](schema-mbnprofile-element.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/> |
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

 

 




