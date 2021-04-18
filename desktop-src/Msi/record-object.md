---
description: L'oggetto record è un contenitore per la conservazione e il trasferimento di un numero variabile di valori.
ms.assetid: e832c19f-61a6-4e42-a10a-b7bb1705af59
title: Oggetto record
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c13cb31d628525e529491af1c089555ba2ad8273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329953"
---
# <a name="record-object"></a>Oggetto record

L'oggetto **record** è un contenitore per la conservazione e il trasferimento di un numero variabile di valori. I campi all'interno del record sono indicizzati numericamente e possono contenere stringhe, numeri interi, oggetti e valori null. I campi che superano le dimensioni del record allocato vengono considerati come aventi valori null permanenti. Il campo numero 0 è riservato.

## <a name="members"></a>Membri

L'oggetto **record** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **record** presenta questi metodi.



| Metodo                                  | Descrizione                                                                                          |
|:----------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**ClearData**](record-cleardata.md)   | Cancella i dati in tutti i campi e li imposta su null.<br/>                                      |
| [**FormatText**](record-formattext.md) | Formatta i campi in base al modello nel campo 0.<br/>                                      |
| [**ReadStream**](record-readstream.md) | Legge un numero specificato di byte da un campo record contenente dati di flusso.<br/>                |
| [**Sestream**](record-setstream.md)   | Copia il contenuto del file specificato nel campo record designato come dati di flusso.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **record** dispone di queste proprietà.



| Proprietà                                             | Tipo di accesso           | Descrizione                                                                                   |
|:-----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [**DataSize**](record-datasize.md)<br/>       |                       | Restituisce la dimensione dei dati per il campo designato.<br/>                             |
| [**FieldCount**](record-fieldcount.md)<br/>   |                       | Restituisce il numero di campi presenti nel record.<br/>                                        |
| [**IntegerData**](record-integerdata.md)<br/> | Lettura/Scrittura<br/> | Trasferisce i dati Integer a 32 bit all'interno o all'esterno di un campo specificato all'interno del record.<br/> |
| [**IsNull**](record-isnull.md)<br/>           |                       | Restituisce true se il campo indicato è null e false se il campo contiene dati.<br/>  |
| [**StringData**](record-stringdata.md)<br/>   | Lettura/Scrittura<br/> | Trasferisce i dati stringa in o da un campo specificato all'interno del record.<br/>         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord è definito come 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo CreaRecord**](installer-createrecord.md)
</dt> <dt>

[Esempi di script di Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




