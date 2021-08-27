---
description: Fornisce informazioni ai metodi dell'interfaccia IQueryAssociations.
ms.assetid: e67d0282-9090-43e6-aedf-bb1fc0443221
title: Enumerazione ASSOCF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d52de3ce181033358fc20ca3e4f8759b61f72ed
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786697"
---
# <a name="assocf-enumeration"></a>Enumerazione ASSOCF

Fornisce informazioni ai metodi [**dell'interfaccia IQueryAssociations.**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations)

## <a name="syntax"></a>Sintassi




| C++ | 
|-----|
| <pre><code>typedef enum  {   ASSOCF_NONE                  = 0x00000000,  ASSOCF_INIT_NOREMAPCLSID     = 0x00000001,  ASSOCF_INIT_BYEXENAME        = 0x00000002,  ASSOCF_OPEN_BYEXENAME        = 0x00000002,  ASSOCF_INIT_DEFAULTTOSTAR    = 0x00000004,  ASSOCF_INIT_DEFAULTTOFOLDER  = 0x00000008,  ASSOCF_NOUSERSETTINGS        = 0x00000010,  ASSOCF_NOTRUNCATE            = 0x00000020,  ASSOCF_VERIFY                = 0x00000040,  ASSOCF_REMAPRUNDLL           = 0x00000080,  ASSOCF_NOFIXUPS              = 0x00000100,  ASSOCF_IGNOREBASECLASS       = 0x00000200,  ASSOCF_INIT_IGNOREUNKNOWN    = 0x00000400,  ASSOCF_INIT_FIXED_PROGID     = 0x00000800,  ASSOCF_IS_PROTOCOL           = 0x00001000,  ASSOCF_INIT_FOR_FILE         = 0x00002000} ASSOCF;</code></pre> | 




## <a name="constants"></a>Costanti

 <span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF \_ NONE** 

Nessuna delle opzioni seguenti è impostata.

 <span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF \_ INIT \_ NOREMAPCLSID** 

Indica ai metodi [**dell'interfaccia IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) di non eseguire il mapping dei valori CLSID ai valori ProgID.

 <span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF \_ INIT \_ BYEXENAME** 

Identifica il valore del *parametro pwszAssoc* di [**IQueryAssociations::Init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) come nome di file eseguibile. Se questo flag non è impostato, la chiave radice verrà impostata sul ProgID associato alla chiave **.exe** anziché sul ProgID del file eseguibile.

 <span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF \_ OPEN \_ BYEXENAME** 

Identico a **ASSOCF \_ INIT \_ BYEXENAME**.

 <span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF \_ INIT \_ DEFAULTTOSTAR** 

Specifica che quando un [**metodo IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) non trova il valore richiesto nella chiave radice, deve tentare di recuperare il valore confrontabile dalla **\*** sottochiave.

 <span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF \_ INIT \_ DEFAULTTOFOLDER** 

Specifica che quando un [**metodo IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) non trova il valore richiesto nella chiave radice, deve tentare di recuperare il valore confrontabile dalla sottochiave **Folder.**

 <span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**ASSOCF \_ NOUSERSETTINGS** 

Specifica che è necessario cercare **solo HKEY \_ CLASSES \_ ROOT** e **che HKEY CURRENT \_ \_ USER** deve essere ignorato.

 <span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF \_ NOTRUNCATE** 

Specifica che la stringa restituita non deve essere troncata. Restituire invece un valore di errore e le dimensioni necessarie per la stringa completa.

 <span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**VERIFICA DI \_ ASSOCF** 

Indica ai metodi [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) di verificare che i dati siano accurati. Questa impostazione consente **ai metodi IQueryAssociations** di leggere i dati dal disco rigido dell'utente per la verifica. Ad esempio, possono controllare il nome descrittivo nel Registro di sistema rispetto a quello archiviato nel file .exe file. L'impostazione di questo flag riduce in genere l'efficienza del metodo .

 <span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**REMAPRUNDLL DI ASSOCF \_** 

Indica ai metodi [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) di ignorare Rundll.exe e restituire informazioni sulla destinazione. In genere **i metodi IQueryAssociations** restituiscono informazioni sulla prima .exe o .dll in una stringa di comando. Se un comando usa Rundll.exe, l'impostazione di questo flag indica al metodo di ignorare Rundll.exe e restituire informazioni sulla destinazione.

 <span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**NOFIXUPS DI ASSOCF \_** 

Indica ai metodi [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) di non correggere gli errori nel Registro di sistema, ad esempio il nome descrittivo di una funzione che non corrisponde a quello trovato nel file .exe.

 <span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**ASSOCF \_ IGNOREBASECLASS** 

Specifica che il valore BaseClass deve essere ignorato.

 <span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF \_ INIT \_ IGNOREUNKNOWN** 

**Introdotto in Windows 7**. Specifica che il ProgID "Sconosciuto" deve essere ignorato. al contrario, ha esito negativo.

 <span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**\_PROGID FISSO ASSOCF INIT \_ \_** 

**Introdotto in Windows 8**. Specifica che il ProgID fornito deve essere mappato usando le impostazioni predefinite del sistema, anziché le impostazioni predefinite dell'utente corrente.

 <span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**PROTOCOLLO ASSOCF \_ \_ IS** 

**Introdotto in Windows 8**. Specifica che il valore è un protocollo e deve essere mappato usando le impostazioni predefinite dell'utente corrente.

 <span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF \_ INIT \_ PER \_ FILE** 

**Introdotto in Windows 8.1**. Specifica che ProgID corrisponde a un'associazione basata su estensione di file. Usare insieme a **ASSOCF \_ INIT \_ FIXED \_ PROGID**.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 2000 Professional, Windows solo app \[ desktop XP\]               |
| Server minimo supportato | Windows 2000 Server \[solo app desktop\]                                 |
| Intestazione                   |  Shlwapi.h  |



## <a name="see-also"></a>Vedi anche

 [**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) 

 

 

© 2017 Microsoft. Tutti i diritti sono riservati.
