---
description: Specifica un percorso di file che rappresenta un percorso di archiviazione che il modulo di decrittografia di contenuto (CDM) può usare per l'inizializzazione.
title: MF_CONTENTDECRYPTIONMODULE_STOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 8126bfea15f9946bb9950293a6c39c101f9c37c8870176fb4bb0108aa5862bb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723461"
---
# <a name="mf_contentdecryptionmodule_storepath-property"></a>MF \_ CONTENTDECRYPTIONMODULE \_ - proprietà STOREPATH

Specifica un percorso di file che rappresenta un percorso di archiviazione che il modulo di decrittografia di contenuto (CDM) può usare per l'inizializzazione.


## <a name="data-type"></a>Tipo di dati

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>GUID proprietà

**MF \_ CONTENTDECRYPTIONMODULE \_ STOREPATH**

## <a name="property-value"></a>Valore proprietà

Percorso di file che rappresenta un percorso di archiviazione che il modulo di decrittografia di contenuto (CDM) può usare per l'inizializzazione.

## <a name="remarks"></a>Commenti

Il percorso specificato con questa proprietà verrà usato anche per i dati specifici del contenuto se la MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH [proprietà](mf-contentdecryptionmodule-inprivatestorepath.md) non è impostata.

Per migliorare le prestazioni COM, l'app non deve eliminare la posizione dello Store dopo il rilascio dell'oggetto CDM.



Impostare questa proprietà quando si crea un cdm chiamando [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10 Aggiornamento di aprile 2020<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>mfcontentdecryptionmodule.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

- [Media Foundation proprietà](media-foundation-properties.md)
- [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




