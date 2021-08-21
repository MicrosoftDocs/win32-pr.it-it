---
description: Identifica una voce nel database shim.
ms.assetid: c092592d-a4f4-4b2f-9b03-c07951ed214a
title: TAG (Exposeenums2managed.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7e4df727245ead30ecefef0cd941148b8f4c76e2881ab19f41c3388934abd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075795"
---
# <a name="tag"></a>ETICHETTA

Identifica una voce nel database shim.

Le voci seguenti sono di tipo **TAG \_ TYPE \_ LIST** (0x7000).



| Costante/valore                                                                                                                                                                                                                                                             | Descrizione                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| <span id="TAG_DATABASE"></span><span id="tag_database"></span><dl> <dt>**TAG \_ DATABASE**</dt> <dt>(0x1 \| **ELENCO DEI TIPI DI \_ \_ TAG**)</dt> </dl>                               | Voce di database.<br/>                                                |
| <span id="TAG_LIBRARY"></span><span id="tag_library"></span><dl> <dt>**TAG \_ LIBRARY**</dt> <dt>(0x2 \| **ELENCO DEI TIPI DI \_ \_ TAG**)</dt> </dl>                                  | Voce libreria.<br/>                                                 |
| <span id="TAG_INEXCLUDE"></span><span id="tag_inexclude"></span><dl> <dt>**TAG \_ INEXCLUDE**</dt> <dt>(0x3 \| **TIPO DI TAG \_ \_ LIST**)</dt> </dl>                            | Includere ed escludere una voce.<br/>                                     |
| <span id="TAG_SHIM"></span><span id="tag_shim"></span><dl> <dt>**TAG \_ SHIM**</dt> <dt>(0x4 \| **TIPO DI TAG \_ \_ LIST**)</dt> </dl>                                           | Voce Shim che contiene le informazioni sul nome e sullo scopo.<br/>     |
| <span id="TAG_PATCH"></span><span id="tag_patch"></span><dl> <dt>**TAG \_ PATCH**</dt> <dt>(0x5 \| **TIPO DI TAG \_ \_ LIST**)</dt> </dl>                                        | Voce patch che contiene le informazioni sull'applicazione di patch in memoria.<br/>  |
| <span id="TAG_APP"></span><span id="tag_app"></span><dl> <dt>**TAG \_ APP**</dt> <dt>(0x6 \| **ELENCO \_ DEI TIPI \_ DI TAG**)</dt> </dl>                                              | Voce dell'applicazione.<br/>                                             |
| <span id="TAG_EXE"></span><span id="tag_exe"></span><dl> <dt>**TAG \_ EXE**</dt> <dt>(0x7 \| **ELENCO DEI TIPI DI \_ \_ TAG**)</dt> </dl>                                              | Voce eseguibile.<br/>                                              |
| <span id="TAG_MATCHING_FILE"></span><span id="tag_matching_file"></span><dl> <dt>**TAG \_ MATCHING \_ FILE**</dt> <dt>(0X8 \| **TAG TYPE \_ \_ LIST**)</dt> </dl>               | Voce del file corrispondente.<br/>                                           |
| <span id="TAG_SHIM_REF"></span><span id="tag_shim_ref"></span><dl> <dt>**TAG \_ SHIM \_ REF**</dt> <dt>(elenco 0x9 TIPO DI \| \_ \_ TAG)</dt> </dl>                                   | Voce di definizione shim.<br/>                                         |
| <span id="TAG_PATCH_REF"></span><span id="tag_patch_ref"></span><dl> <dt>**TAG \_ PATCH \_ REF**</dt> <dt>(0xA TAG TYPE \| **\_ \_ LIST**)</dt> </dl>                           | Voce di definizione della patch.<br/>                                        |
| <span id="TAG_LAYER"></span><span id="tag_layer"></span><dl> <dt>**TAG \_ LAYER**</dt> <dt>(0xB \| **TAG TYPE \_ \_ LIST**)</dt> </dl>                                        | Voce dello shim di livello.<br/>                                              |
| <span id="TAG_FILE"></span><span id="tag_file"></span><dl> <dt>**TAG \_ FILE**</dt> <dt>(0xC \| **ELENCO DEI TIPI DI \_ \_ TAG**)</dt> </dl>                                           | Attributo di file utilizzato in una voce shim.<br/>                           |
| <span id="TAG_APPHELP"></span><span id="tag_apphelp"></span><dl> <dt>**TAG \_ APPHELP**</dt> <dt>(0xD \| **TIPO DI TAG \_ \_ LIST**)</dt> </dl>                                  | Voce di informazioni apphelp.<br/>                                     |
| <span id="TAG_LINK"></span><span id="tag_link"></span><dl> <dt>**TAG \_ LINK**</dt> <dt>(0xE \| **TIPO DI TAG \_ \_ LIST**)</dt> </dl>                                           | Voce di informazioni sul collegamento online Apphelp.<br/>                         |
| <span id="TAG_DATA"></span><span id="tag_data"></span><dl> <dt>**TAG \_ DATA**</dt> <dt>(0xF \| **TAG \_ TYPE \_ LIST**)</dt> </dl>                                           | Voce di mapping nome-valore.<br/>                                      |
| <span id="TAG_MSI_TRANSFORM"></span><span id="tag_msi_transform"></span><dl> <dt>**TAG \_ MSI \_ TRANSFORM**</dt> <dt>(0X10 \| **TAG TYPE \_ \_ LIST**)</dt> </dl>              | Voce di trasformazione MSI.<br/>                                      |
| <span id="TAG_MSI_TRANSFORM_REF"></span><span id="tag_msi_transform_ref"></span><dl> <dt>**TAG \_ MSI \_ TRANSFORM \_ REF (0X11**</dt> TAG TYPE <dt> \| **\_ \_ LIST**)</dt> </dl> | Voce di definizione della trasformazione MSI.<br/>                           |
| <span id="TAG_MSI_PACKAGE"></span><span id="tag_msi_package"></span><dl> <dt>**TAG \_ PACCHETTO \_ MSI**</dt> <dt>(0x12 \| **ELENCO DEI TIPI DI \_ \_ TAG**)</dt> </dl>                    | Voce del pacchetto MSI.<br/>                                             |
| <span id="TAG_FLAG"></span><span id="tag_flag"></span><dl> <dt>**TAG \_ FLAG**</dt> <dt>(0x13 \| **ELENCO \_ DI TIPI \_ DI TAG**)</dt> </dl>                                          | Voce del flag.<br/>                                                    |
| <span id="TAG_MSI_CUSTOM_ACTION"></span><span id="tag_msi_custom_action"></span><dl> <dt>**TAG \_ AZIONE \_ PERSONALIZZATA \_ MSI**</dt> <dt>(elenco 0x14 TIPO DI TAG \| **\_ \_ MSI**)</dt> </dl> | Voce dell'azione personalizzata MSI.<br/>                                       |
| <span id="TAG_FLAG_REF"></span><span id="tag_flag_ref"></span><dl> <dt>**TAG \_ FLAG \_ REF**</dt> <dt>(0x15 TAG TYPE \| **\_ \_ LIST**)</dt> </dl>                             | Voce di definizione del flag.<br/>                                         |
| <span id="TAG_ACTION"></span><span id="tag_action"></span><dl> <dt>**TAG \_ ACTION**</dt> <dt>(0x16 \| **TAG \_ TYPE \_ LIST**)</dt> </dl>                                    | Non utilizzato.<br/>                                                        |
| <span id="TAG_LOOKUP"></span><span id="tag_lookup"></span><dl> <dt>**TAG \_ LOOKUP**</dt> <dt>(0x17 \| **TIPO DI TAG \_ \_ LIST**)</dt> </dl>                                    | Voce di ricerca utilizzata per la ricerca in un database driver.<br/>             |
| <span id="TAG_STRINGTABLE"></span><span id="tag_stringtable"></span><dl> <dt>**TAG \_ STRINGTABLE**</dt> <dt>(0x801 \| **TIPO DI TAG \_ \_ LIST**)</dt> </dl>                    | Voce della tabella di stringhe.<br/>                                            |
| <span id="TAG_INDEXES"></span><span id="tag_indexes"></span><dl> <dt>**TAG \_ INDEXES**</dt> <dt>(0x802 \| **TAG \_ TYPE \_ LIST**)</dt> </dl>                                | Voce di indice che definisce tutti gli indici in un database shim.<br/> |
| <span id="TAG_INDEX"></span><span id="tag_index"></span><dl> <dt>**TAG \_ INDEX**</dt> <dt>(0x803 \| **TIPO DI TAG \_ \_ LIST**)</dt> </dl>                                      | Voce di indice che definisce un indice in un database shim.<br/>          |



Le voci seguenti sono di tipo **TAG \_ TYPE \_ STRINGREF** (0x6000).



| Costante/valore                                                                                                                                                                                                                                                                     | Descrizione                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="TAG_NAME"></span><span id="tag_name"></span><dl> <dt>**TAG \_ NAME**</dt> <dt>(0x1 \| **TIPO \_ DI TAG \_ STRINGREF**)</dt> </dl>                                              | Attributo Name.<br/>                                                                    |
| <span id="TAG_DESCRIPTION"></span><span id="tag_description"></span><dl> <dt>**TAG \_ DESCRIPTION**</dt> <dt>(0x2 \| **TIPO DI TAG \_ \_ STRINGREF**)</dt> </dl>                         | Descrizione.<br/>                                                                 |
| <span id="TAG_MODULE"></span><span id="tag_module"></span><dl> <dt>**TAG \_ MODULE**</dt> <dt>(0x3 \| **TIPO DI TAG \_ \_ STRINGREF**)</dt> </dl>                                        | Attributo module.<br/>                                                                  |
| <span id="TAG_API"></span><span id="tag_api"></span><dl> <dt>**TAG \_ API**</dt> <dt>(0x4 \| **TIPO DI TAG \_ \_ STRINGREF**)</dt> </dl>                                                 | Voce API.<br/>                                                                         |
| <span id="TAG_VENDOR"></span><span id="tag_vendor"></span><dl> <dt>**TAG \_ VENDOR**</dt> <dt>(0x5 \| **TIPO \_ DI TAG \_ STRINGREF**)</dt> </dl>                                        | Attributo del nome del fornitore.<br/>                                                             |
| <span id="TAG_APP_NAME"></span><span id="tag_app_name"></span><dl> <dt>**TAG \_ NOME \_ APP**</dt> <dt>(0X6 \| **TIPO DI TAG \_ \_ STRINGREF**)</dt> </dl>                                 | Attributo del nome dell'applicazione che descrive una voce dell'applicazione in un database shim.<br/> |
| <span id="TAG_COMMAND_LINE"></span><span id="tag_command_line"></span><dl> <dt>**TAG \_ RIGA \_ DI COMANDO**</dt> <dt>(0X8 TIPO DI TAG \| **\_ \_ STRINGREF**)</dt> </dl>                     | Attributo della riga di comando usato, ad esempio, quando si passano argomenti a uno shim.<br/> |
| <span id="TAG_COMPANY_NAME"></span><span id="tag_company_name"></span><dl> <dt>**TAG \_ NOME \_ SOCIETÀ**</dt> <dt>(0X9 \| **TIPO DI TAG \_ \_ STRINGREF**)</dt> </dl>                     | Attributo nome società.<br/>                                                            |
| <span id="TAG_DLLFILE"></span><span id="tag_dllfile"></span><dl> <dt>**TAG \_ DLLFILE**</dt> <dt>(0xA \| **TIPO DI TAG \_ \_ STRINGREF**)</dt> </dl>                                     | Attributo del file DLL per una voce shim.<br/>                                               |
| <span id="TAG_WILDCARD_NAME"></span><span id="tag_wildcard_name"></span><dl> <dt>**TAG \_ NOME \_ CON CARATTERI**</dt> JOLLY <dt>(0xB TIPO DI TAG \| **\_ \_ STRINGREF**)</dt> </dl>                  | Attributo del nome con caratteri jolly per una voce eseguibile con un carattere jolly come nome file.<br/>  |
| <span id="TAG_PRODUCT_NAME"></span><span id="tag_product_name"></span><dl> <dt>**TAG \_ NOME \_ PRODOTTO**</dt> <dt>(0X10 \| **TIPO DI TAG \_ \_ STRINGREF**)</dt> </dl>                    | Attributo del nome del prodotto.<br/>                                                            |
| <span id="TAG_PRODUCT_VERSION"></span><span id="tag_product_version"></span><dl> <dt>**TAG \_ PRODUCT \_ VERSION**</dt> <dt>(0X11 TIPO DI TAG \| **\_ \_ STRINGREF**)</dt> </dl>           | Attributo della versione del prodotto.<br/>                                                         |
| <span id="TAG_FILE_DESCRIPTION"></span><span id="tag_file_description"></span><dl> <dt>**TAG \_ DESCRIZIONE \_ FILE**</dt> <dt>(0x12 \| **TIPO DI TAG \_ \_ STRINGREF**)</dt> </dl>        | Attributo di descrizione del file.<br/>                                                        |
| <span id="TAG_FILE_VERSION"></span><span id="tag_file_version"></span><dl> <dt>**TAG \_ VERSIONE \_ FILE**</dt> <dt>(0X13 \| **TIPO DI TAG \_ \_ STRINGREF**)</dt> </dl>                    | Attributo della versione del file.<br/>                                                            |
| <span id="TAG_ORIGINAL_FILENAME"></span><span id="tag_original_filename"></span><dl> <dt>**TAG \_ NOME \_ FILE ORIGINALE**</dt> <dt>(0X14 TIPO DI TAG \| **\_ \_ STRINGREF**)</dt> </dl>     | Attributo del nome file originale.<br/>                                                      |
| <span id="TAG_INTERNAL_NAME"></span><span id="tag_internal_name"></span><dl> <dt>**TAG \_ NOME \_ INTERNO**</dt> <dt>(0X15 TIPO DI TAG \| **\_ \_ STRINGREF**)</dt> </dl>                 | Attributo interno del nome file.<br/>                                                      |
| <span id="TAG_LEGAL_COPYRIGHT"></span><span id="tag_legal_copyright"></span><dl> <dt>**TAG \_ \_COPYRIGHT LEGALE**</dt> <dt>(0X16 \| **TIPO DI TAG \_ \_ STRINGREF**)</dt> </dl>           | Attributo copyright.<br/>                                                               |
| <span id="TAG_16BIT_DESCRIPTION"></span><span id="tag_16bit_description"></span><dl> <dt>**TAG \_ DESCRIZIONE \_ A 16 BIT**</dt> <dt>(0X17 TIPO DI TAG \| **\_ \_ STRINGREF**)</dt> </dl>     | Attributo description a 16 bit.<br/>                                                      |
| <span id="TAG_APPHELP_DETAILS"></span><span id="tag_apphelp_details"></span><dl> <dt>**TAG \_ DETTAGLI \_ APPHELP**</dt> <dt>(0X18 \| **TIPO DI TAG \_ \_ STRINGREF**)</dt> </dl>           | Attributo delle informazioni del messaggio dei dettagli di Apphelp.<br/>                                     |
| <span id="TAG_LINK_URL"></span><span id="tag_link_url"></span><dl> <dt>**TAG \_ \_URL COLLEGAMENTO**</dt> <dt>(0x19 TIPO DI TAG \| **\_ \_ STRINGREF**)</dt> </dl>                                | Attributo URL collegamento online apphelp.<br/>                                                 |
| <span id="TAG_LINK_TEXT"></span><span id="tag_link_text"></span><dl> <dt>**TAG \_ LINK \_ TEXT**</dt> <dt>(0X1A \| **TIPO DI TAG \_ \_ STRINGREF**)</dt> </dl>                             | Attributo di testo del collegamento online apphelp.<br/>                                                |
| <span id="TAG_APPHELP_TITLE"></span><span id="tag_apphelp_title"></span><dl> <dt>**TAG \_ APPHELP \_ TITLE**</dt> <dt>(0X1B \| **TIPO DI TAG \_ \_ STRINGREF**)</dt> </dl>                 | Attributo del titolo apphelp.<br/>                                                           |
| <span id="TAG_APPHELP_CONTACT"></span><span id="tag_apphelp_contact"></span><dl> <dt>**TAG \_ CONTATTO \_ APPHELP**</dt> <dt>(0X1C \| **TIPO DI TAG \_ \_ STRINGREF**)</dt> </dl>           | Attributo di contatto del fornitore apphelp.<br/>                                                  |
| <span id="TAG_SXS_MANIFEST"></span><span id="tag_sxs_manifest"></span><dl> <dt>**TAG \_ MANIFESTO \_ SXS**</dt> <dt>(0x1D \| **TIPO DI TAG \_ \_ STRINGREF**)</dt> </dl>                    | Voce del manifesto side-by-side.<br/>                                                       |
| <span id="TAG_DATA_STRING"></span><span id="tag_data_string"></span><dl> <dt>**TAG \_ STRINGA \_ DI DATI**</dt> <dt>(0X1E TIPO DI TAG \| **\_ \_ STRINGREF**)</dt> </dl>                       | Attributo stringa per un'immissione di dati.<br/>                                                 |
| <span id="TAG_MSI_TRANSFORM_FILE"></span><span id="tag_msi_transform_file"></span><dl> <dt>**TAG \_ \_FILE DI TRASFORMAZIONE \_ MSI**</dt> <dt>(0X1F TIPO DI TAG \| **\_ \_ STRINGREF**)</dt> </dl> | Attributo del nome file di una voce di trasformazione MSI.<br/>                                |
| <span id="TAG_16BIT_MODULE_NAME"></span><span id="tag_16bit_module_name"></span><dl> <dt>**TAG \_ 16BIT \_ MODULE \_ NAME**</dt> <dt>(0X20 TAG TYPE \| **\_ \_ STRINGREF**)</dt> </dl>    | Attributo del nome del modulo a 16 bit.<br/>                                                      |
| <span id="TAG_LAYER_DISPLAYNAME"></span><span id="tag_layer_displayname"></span><dl> <dt>**TAG \_ LAYER \_ DISPLAYNAME**</dt> <dt>(0X21 \| **TIPO DI TAG \_ \_ STRINGREF**)</dt> </dl>     | Non utilizzato.<br/>                                                                            |
| <span id="TAG_COMPILER_VERSION"></span><span id="tag_compiler_version"></span><dl> <dt>**TAG \_ VERSIONE \_ DEL COMPILATORE**</dt> <dt>(0X22 TIPO DI TAG \| **\_ \_ STRINGREF**)</dt> </dl>        | Versione del compilatore di database Shim.<br/>                                                    |
| <span id="TAG_ACTION_TYPE"></span><span id="tag_action_type"></span><dl> <dt>**TAG \_ TIPO \_ DI AZIONE**</dt> <dt>(0x23 TIPO DI TAG \| **\_ \_ STRINGREF**)</dt> </dl>                       | Non utilizzato.<br/>                                                                            |
| <span id="TAG_EXPORT_NAME"></span><span id="tag_export_name"></span><dl> <dt>**TAG \_ NOME \_ ESPORTAZIONE**</dt> <dt>(0X24 \| **TIPO DI TAG \_ \_ STRINGREF**)</dt> </dl>                       | Attributo nome file di esportazione.<br/>                                                        |



Le voci seguenti sono di tipo **TAG \_ TYPE \_ DWORD** (0x4000).



| Costante/valore                                                                                                                                                                                                                                                                    | Descrizione                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| <span id="TAG_SIZE"></span><span id="tag_size"></span><dl> <dt>**TAG \_ SIZE**</dt> <dt>(0x1 \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>                                                 | Attributo delle dimensioni del file.<br/>                                                                                  |
| <span id="TAG_OFFSET"></span><span id="tag_offset"></span><dl> <dt>**TAG \_ OFFSET**</dt> <dt>(0x2 \| **TIPO DI TAG \_ \_ DWORD**)</dt> </dl>                                           | Non utilizzato.<br/>                                                                                               |
| <span id="TAG_CHECKSUM"></span><span id="tag_checksum"></span><dl> <dt>**TAG \_ CHECKSUM**</dt> <dt>(0x3 \| **TIPO DI TAG \_ \_ DWORD**)</dt> </dl>                                     | Attributo checksum del file.<br/>                                                                              |
| <span id="TAG_SHIM_TAGID"></span><span id="tag_shim_tagid"></span><dl> <dt>**TAG \_ SHIM \_ TAGID**</dt> <dt>(0x4 \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>                              | Attributo **TAGID Shim.**<br/>                                                                             |
| <span id="TAG_PATCH_TAGID"></span><span id="tag_patch_tagid"></span><dl> <dt>**TAG \_ PATCH \_ TAGID**</dt> <dt>(0x5 \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>                           | Attributo **TAGID** patch.<br/>                                                                            |
| <span id="TAG_MODULE_TYPE"></span><span id="tag_module_type"></span><dl> <dt>**TAG \_ MODULE \_ TYPE**</dt> <dt>(0X6 TAG TYPE \| **\_ \_ DWORD**)</dt> </dl>                           | Attributo del tipo di modulo.<br/>                                                                                |
| <span id="TAG_VERDATEHI"></span><span id="tag_verdatehi"></span><dl> <dt>**TAG \_ VERDATEHI**</dt> <dt>(0x7 \| **TAG TYPE \_ \_ DWORD**)</dt> </dl>                                  | Parte di ordine elevato dell'attributo data della versione del file.<br/>                                                |
| <span id="TAG_VERDATELO"></span><span id="tag_verdatelo"></span><dl> <dt>**TAG \_ VERDATELO**</dt> <dt>(0x8 \| **TAG TYPE \_ \_ DWORD**)</dt> </dl>                                  | Parte in ordine ridotto dell'attributo data della versione del file.<br/>                                                 |
| <span id="TAG_VERFILEOS"></span><span id="tag_verfileos"></span><dl> <dt>**TAG \_ VERFILEOS**</dt> <dt>(0x9 \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>                                  | Attributo della versione del file del sistema operativo.<br/>                                                              |
| <span id="TAG_VERFILETYPE"></span><span id="tag_verfiletype"></span><dl> <dt>**TAG \_ VERFILETYPE**</dt> <dt>(0xA \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>                            | Attributo del tipo di file.<br/>                                                                                  |
| <span id="TAG_PE_CHECKSUM"></span><span id="tag_pe_checksum"></span><dl> <dt>**TAG \_ PE \_ CHECKSUM**</dt> <dt>(0xB \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>                           | Attributo checksum del file PE.<br/>                                                                           |
| <span id="TAG_PREVOSMAJORVER"></span><span id="tag_prevosmajorver"></span><dl> <dt>**TAG \_ PREVOSMAJORVER**</dt> <dt>(0xC \| **TIPO DI TAG \_ \_ DWORD**)</dt> </dl>                   | Attributo della versione principale del sistema operativo.<br/>                                                             |
| <span id="TAG_PREVOSMINORVER"></span><span id="tag_prevosminorver"></span><dl> <dt>**TAG \_ PREVOSMINORVER**</dt> <dt>(0xD \| **TAG TYPE \_ \_ DWORD**)</dt> </dl>                   | Attributo di versione del sistema operativo secondario.<br/>                                                             |
| <span id="TAG_PREVOSPLATFORMID"></span><span id="tag_prevosplatformid"></span><dl> <dt>**TAG \_ PREVOSPLATFORMID**</dt> <dt>(0xE \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>             | Attributo dell'identificatore della piattaforma del sistema operativo.<br/>                                                       |
| <span id="TAG_PREVOSBUILDNO"></span><span id="tag_prevosbuildno"></span><dl> <dt>**TAG \_ PREVOSBUILDNO**</dt> <dt>(0xF \| **TIPO DI TAG \_ \_ DWORD**)</dt> </dl>                      | Attributo del numero di build del sistema operativo.<br/>                                                              |
| <span id="TAG_PROBLEMSEVERITY"></span><span id="tag_problemseverity"></span><dl> <dt>**TAG \_ PROBLEMSEVERITY**</dt> <dt>(0X10 \| **TAG TYPE \_ \_ DWORD**)</dt> </dl>               | Attributo Block di una voce Apphelp. In questo modo si determina se l'applicazione è bloccata in modo rigido o soft.<br/> |
| <span id="TAG_LANGID"></span><span id="tag_langid"></span><dl> <dt>**TAG \_ LANGID**</dt> <dt>(0x11 \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>                                          | Identificatore di lingua di una voce apphelp.<br/>                                                              |
| <span id="TAG_VER_LANGUAGE"></span><span id="tag_ver_language"></span><dl> <dt>**TAG \_ VER \_ LANGUAGE**</dt> <dt>(0x12 TAG TYPE \| **\_ \_ DWORD**)</dt> </dl>                       | Attributo della versione del linguaggio di un file.<br/>                                                                 |
| <span id="TAG_ENGINE"></span><span id="tag_engine"></span><dl> <dt>**TAG \_ ENGINE**</dt> <dt>(0x14 \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>                                          | Non utilizzato.<br/>                                                                                               |
| <span id="TAG_HTMLHELPID"></span><span id="tag_htmlhelpid"></span><dl> <dt>**TAG \_ HTMLHELPID**</dt> <dt>(0x15 \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>                              | Attributo identificatore della Guida per una voce apphelp.<br/>                                                       |
| <span id="TAG_INDEX_FLAGS"></span><span id="tag_index_flags"></span><dl> <dt>**TAG \_ FLAG \_ DI INDICE**</dt> <dt>(0x16 TIPO DI TAG \| **\_ \_ DWORD**)</dt> </dl>                          | Attributo Flags per una voce di indice.<br/>                                                                   |
| <span id="TAG_FLAGS"></span><span id="tag_flags"></span><dl> <dt>**TAG \_ FLAGS**</dt> <dt>(0x17 \| **TIPO DI TAG \_ \_ DWORD**)</dt> </dl>                                             | Attributo Flags per una voce Apphelp.<br/>                                                                 |
| <span id="TAG_DATA_VALUETYPE"></span><span id="tag_data_valuetype"></span><dl> <dt>**TAG \_ DATA \_ VALUETYPE**</dt> <dt>(0X18 \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>                 | Attributo del tipo di dati per un'immissione di dati.<br/>                                                                 |
| <span id="TAG_DATA_DWORD"></span><span id="tag_data_dword"></span><dl> <dt>**TAG \_ DATA \_ DWORD**</dt> <dt>(0x19 \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>                             | **Attributo del valore DWORD** per un'immissione di dati.<br/>                                                           |
| <span id="TAG_LAYER_TAGID"></span><span id="tag_layer_tagid"></span><dl> <dt>**TAG \_ LAYER \_ TAGID**</dt> <dt>(0x1A \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>                          | Attributo **TAGID dello** shim di livello.<br/>                                                                       |
| <span id="TAG_MSI_TRANSFORM_TAGID"></span><span id="tag_msi_transform_tagid"></span><dl> <dt>**TAG \_ MSI \_ TRANSFORM \_ TAGID**</dt> <dt>(0x1B TAG TYPE \| **\_ \_ DWORD**)</dt> </dl> | Attributo **TAGID di trasformazione** MSI.<br/>                                                                    |
| <span id="TAG_LINKER_VERSION"></span><span id="tag_linker_version"></span><dl> <dt>**TAG \_ VERSIONE DEL \_ LINKER**</dt> <dt>(0x1C \| **TIPO DI TAG \_ \_ DWORD**)</dt> </dl>                 | Attributo di versione del linker di un file.<br/>                                                                   |
| <span id="TAG_LINK_DATE"></span><span id="tag_link_date"></span><dl> <dt>**TAG \_ LINK \_ DATE**</dt> <dt>(0X1D \| **TAG TYPE \_ \_ DWORD**)</dt> </dl>                                | Attributo data di collegamento di un file.<br/>                                                                        |
| <span id="TAG_UPTO_LINK_DATE"></span><span id="tag_upto_link_date"></span><dl> <dt>**TAG \_ UPTO \_ LINK \_ DATE**</dt> <dt>(0X1E TAG TYPE \| **\_ \_ DWORD**)</dt> </dl>                | Attributo data di collegamento di un file. La corrispondenza viene eseguita fino a questa data di collegamento e inclusa.<br/>                   |
| <span id="TAG_OS_SERVICE_PACK"></span><span id="tag_os_service_pack"></span><dl> <dt>**TAG \_ SERVICE \_ \_ PACK DEL SISTEMA OPERATIVO**</dt> <dt>(0x1F TIPO DI TAG \| **\_ \_ DWORD**)</dt> </dl>             | Attributo del Service Pack del sistema operativo per una voce eseguibile.<br/>                                      |
| <span id="TAG_FLAG_TAGID"></span><span id="tag_flag_tagid"></span><dl> <dt>**TAG \_ FLAG \_ TAGID**</dt> <dt>(0x20 \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>                             | Contrassegna **l'attributo TAGID.**<br/>                                                                            |
| <span id="TAG_RUNTIME_PLATFORM"></span><span id="tag_runtime_platform"></span><dl> <dt>**TAG \_ PIATTAFORMA \_ DI**</dt> <dt>RUNTIME (0X21 TIPO DI TAG \| **\_ \_ DWORD**)</dt> </dl>           | Attributo della piattaforma di run-time di un file.<br/>                                                                |
| <span id="TAG_OS_SKU"></span><span id="tag_os_sku"></span><dl> <dt>**TAG \_ SKU \_ del sistema operativo**</dt> <dt>(0x22 TIPO DI TAG \| **\_ \_ DWORD**)</dt> </dl>                                         | Attributo SKU del sistema operativo per una voce eseguibile.<br/>                                               |
| <span id="TAG_OS_PLATFORM"></span><span id="tag_os_platform"></span><dl> <dt>**TAG \_ PIATTAFORMA DEL \_ SISTEMA OPERATIVO**</dt> <dt>(0X23 TIPO DI TAG \| **\_ \_ DWORD**)</dt> </dl>                          | Attributo della piattaforma del sistema operativo.<br/>                                                                  |
| <span id="TAG_APP_NAME_RC_ID"></span><span id="tag_app_name_rc_id"></span><dl> <dt>**TAG \_ APP \_ NAME \_ RC \_ ID**</dt> <dt>(0x24 TAG TYPE \| **\_ \_ DWORD**)</dt> </dl>               | Attributo dell'identificatore di risorsa del nome dell'applicazione per le voci di Apphelp.<br/>                                   |
| <span id="TAG_VENDOR_NAME_RC_ID"></span><span id="tag_vendor_name_rc_id"></span><dl> <dt>**TAG \_ VENDOR \_ NAME \_ RC \_ ID**</dt> <dt>(0X25 TAG TYPE \| **\_ \_ DWORD**)</dt> </dl>      | Attributo dell'identificatore di risorsa del nome del fornitore per le voci di Apphelp.<br/>                                        |
| <span id="TAG_SUMMARY_MSG_RC_ID"></span><span id="tag_summary_msg_rc_id"></span><dl> <dt>**TAG \_ SUMMARY \_ MSG \_ RC \_ ID (0X26**</dt> <dt>TAG TYPE \| **\_ \_ DWORD**)</dt> </dl>      | Attributo dell'identificatore di risorsa del messaggio di riepilogo per le voci di Apphelp.<br/>                                    |
| <span id="TAG_VISTA_SKU"></span><span id="tag_vista_sku"></span><dl> <dt>**TAG \_ \_SKU VISTA**</dt> <dt>(0X27 \| **TIPO DI TAG \_ \_ DWORD**)</dt> </dl>                                | Windows Attributo dello SKU vista.<br/>                                                                          |
| <span id="TAG_DESCRIPTION_RC_ID"></span><span id="tag_description_rc_id"></span><dl> <dt>**TAG \_ ID \_ RC \_ DESCRIZIONE**</dt> <dt>(0x28 \| **TIPO DI TAG \_ \_ DWORD**)</dt> </dl>       | Descrizione dell'attributo dell'identificatore di risorsa per le voci di Apphelp.<br/>                                        |
| <span id="TAG_PARAMETER1_RC_ID"></span><span id="tag_parameter1_rc_id"></span><dl> <dt>**TAG \_ PARAMETER1 \_ RC \_ ID**</dt> <dt>(0X29 \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>          | Attributo dell'identificatore di risorsa Parameter1 per le voci apphelp.<br/>                                         |
| <span id="TAG_TAGID"></span><span id="tag_tagid"></span><dl> <dt>**TAG \_ TAGID**</dt> <dt>(0x801 \| **TIPO DI TAG \_ \_ DWORD**)</dt> </dl>                                            | **Attributo TAGID.**<br/>                                                                                  |



La voce seguente è di tipo **TAG \_ TYPE \_ STRING** (0x8000).



| Costante/valore                                                                                                                                                                                                                                                            | Descrizione                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------|
| <span id="TAG_STRINGTABLE_ITEM"></span><span id="tag_stringtable_item"></span><dl> <dt>**TAG \_ STRINGTABLE \_ ITEM**</dt> <dt>(0X801 \| **TIPO DI TAG \_ \_ STRING**)</dt> </dl> | Voce dell'elemento della tabella di stringhe.<br/> |



Le voci seguenti sono di tipo **TAG \_ TYPE \_ NULL** (0x1000).



| Costante/valore                                                                                                                                                                                                                                                                            | Descrizione                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| <span id="TAG_INCLUDE"></span><span id="tag_include"></span><dl> <dt>**TAG \_ INCLUDE**</dt> <dt>(0x1 \| **TIPO DI TAG \_ \_ NULL**)</dt> </dl>                                                 | Includere la voce dell'elenco.<br/>                           |
| <span id="TAG_GENERAL"></span><span id="tag_general"></span><dl> <dt>**TAG \_ GENERAL**</dt> <dt>(0x2 \| **TAG TYPE \_ \_ NULL**)</dt> </dl>                                                 | Voce shim per utilizzo generico.<br/>                   |
| <span id="TAG_MATCH_LOGIC_NOT"></span><span id="tag_match_logic_not"></span><dl> <dt>**TAG \_ MATCH \_ LOGIC \_ NOT**</dt> <dt>(0X3 TAG TYPE \| **\_ \_ NULL**)</dt> </dl>                       | NOT della voce logica corrispondente.<br/>                  |
| <span id="TAG_APPLY_ALL_SHIMS"></span><span id="tag_apply_all_shims"></span><dl> <dt>**TAG \_ APPLY \_ ALL \_ SMS**</dt> <dt>(0X4 TAG TYPE \| **\_ \_ NULL**)</dt> </dl>                       | Non utilizzato.<br/>                                       |
| <span id="TAG_USE_SERVICE_PACK_FILES"></span><span id="tag_use_service_pack_files"></span><dl> <dt>**TAG \_ USARE \_ I FILE DEL SERVICE \_ PACK \_**</dt> <dt>(0X5 TIPO DI TAG \| **\_ \_ NULL**)</dt> </dl> | Informazioni sul Service Pack per le voci apphelp.<br/> |
| <span id="TAG_MITIGATION_OS"></span><span id="tag_mitigation_os"></span><dl> <dt>**TAG \_ SISTEMA OPERATIVO \_ DI MITIGAZIONE**</dt> <dt>(0x6 \| **TIPO DI TAG \_ \_ NULL**)</dt> </dl>                              | Mitigazione nella voce dell'ambito del sistema operativo.<br/>   |
| <span id="TAG_BLOCK_UPGRADE"></span><span id="tag_block_upgrade"></span><dl> <dt>**TAG \_ BLOCCA \_ AGGIORNAMENTO**</dt> <dt>(0X7 \| **TIPO DI TAG \_ \_ NULL**)</dt> </dl>                              | Voce del blocco di aggiornamento.<br/>                          |
| <span id="TAG_INCLUDEEXCLUDEDLL"></span><span id="tag_includeexcludedll"></span><dl> <dt>**TAG \_ INCLUDEEXCLUDEDLL**</dt> <dt>(0X8 \| **TIPO DI TAG \_ \_ NULL**)</dt> </dl>                   | Voce di inclusione/esclusione dll.<br/>                    |



Le voci seguenti sono di tipo **TAG \_ TYPE \_ QWORD** (0x5000).



| Costante/valore                                                                                                                                                                                                                                                                                   | Descrizione                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TAG_TIME"></span><span id="tag_time"></span><dl> <dt>**TAG \_ TIME**</dt> <dt>(0x1 \| **TAG \_ TYPE \_ QWORD**)</dt> </dl>                                                                | Attributo Time.<br/>                                                                                     |
| <span id="TAG_BIN_FILE_VERSION"></span><span id="tag_bin_file_version"></span><dl> <dt>**TAG \_ VERSIONE \_ FILE \_ BIN**</dt> <dt>(0X2 TIPO DI TAG \| **\_ \_ QWORD**)</dt> </dl>                          | Attributo della versione del file bin per le voci di file.<br/>                                                        |
| <span id="TAG_BIN_PRODUCT_VERSION"></span><span id="tag_bin_product_version"></span><dl> <dt>**TAG \_ VERSIONE \_ PRODOTTO \_ BIN**</dt> <dt>(0X3 TIPO DI TAG \| **\_ \_ QWORD**)</dt> </dl>                 | Attributo della versione del prodotto Bin per le voci di file.<br/>                                                     |
| <span id="TAG_MODTIME"></span><span id="tag_modtime"></span><dl> <dt>**TAG \_ MODTIME**</dt> <dt>(0x4 \| **TAG TYPE \_ \_ QWORD**)</dt> </dl>                                                       | Non utilizzato.<br/>                                                                                             |
| <span id="TAG_FLAG_MASK_KERNEL"></span><span id="tag_flag_mask_kernel"></span><dl> <dt>**TAG \_ KERNEL \_ MASCHERA \_ FLAG**</dt> <dt>(0X5 TIPO DI TAG \| **\_ \_ QWORD**)</dt> </dl>                          | Attributo maschera flag kernel.<br/>                                                                         |
| <span id="TAG_UPTO_BIN_PRODUCT_VERSION"></span><span id="tag_upto_bin_product_version"></span><dl> <dt>**TAG \_ UPTO \_ BIN \_ PRODUCT \_ VERSION**</dt> <dt>(0X6 TAG TYPE \| **\_ \_ QWORD**)</dt> </dl> | Attributo della versione del prodotto Bin di un file. La corrispondenza viene eseguita fino alla versione del prodotto inclusa.<br/> |
| <span id="TAG_DATA_QWORD"></span><span id="tag_data_qword"></span><dl> <dt>**TAG \_ DATA \_ QWORD**</dt> <dt>(0x7 \| **TAG \_ TYPE \_ QWORD**)</dt> </dl>                                             | **Attributo del valore ULONGLONG** per una voce di dati.<br/>                                                     |
| <span id="TAG_FLAG_MASK_USER"></span><span id="tag_flag_mask_user"></span><dl> <dt>**TAG \_ FLAG \_ MASK \_ USER**</dt> <dt>(0X8 TAG TYPE \| **\_ \_ QWORD**)</dt> </dl>                                | Attributo maschera flag utente.<br/>                                                                           |
| <span id="TAG_FLAGS_NTVDM1"></span><span id="tag_flags_ntvdm1"></span><dl> <dt>**TAG \_ FLAGS \_ NTVDM1**</dt> <dt>(0x9 \| **TAG \_ TYPE \_ QWORD**)</dt> </dl>                                       | Attributo maschera flag NTVDM1.<br/>                                                                         |
| <span id="TAG_FLAGS_NTVDM2"></span><span id="tag_flags_ntvdm2"></span><dl> <dt>**TAG \_ FLAGS \_ NTVDM2**</dt> <dt>(0xA \| **TAG \_ TYPE \_ QWORD**)</dt> </dl>                                       | Attributo maschera flag NTVDM2.<br/>                                                                         |
| <span id="TAG_FLAGS_NTVDM3"></span><span id="tag_flags_ntvdm3"></span><dl> <dt>**TAG \_ FLAGS \_ NTVDM3**</dt> <dt>(0xB \| **TAG \_ TYPE \_ QWORD**)</dt> </dl>                                       | Attributo maschera flag NTVDM3.<br/>                                                                         |
| <span id="TAG_FLAG_MASK_SHELL"></span><span id="tag_flag_mask_shell"></span><dl> <dt>**TAG \_ SHELL \_ MASCHERA \_ FLAG**</dt> <dt>(0XC TIPO DI TAG \| **\_ \_ QWORD**)</dt> </dl>                             | Attributo della maschera del flag della shell.<br/>                                                                          |
| <span id="TAG_UPTO_BIN_FILE_VERSION"></span><span id="tag_upto_bin_file_version"></span><dl> <dt>**TAG \_ UPTO \_ BIN \_ FILE \_ VERSION**</dt> <dt>(0XD TAG TYPE \| **\_ \_ QWORD**)</dt> </dl>          | Attributo della versione del file bin di un file. La corrispondenza viene eseguita fino a includere questa versione del file.<br/>       |
| <span id="TAG_FLAG_MASK_FUSION"></span><span id="tag_flag_mask_fusion"></span><dl> <dt>**TAG \_ FLAG \_ MASK \_ FUSION**</dt> <dt>(0XE TAG TYPE \| **\_ \_ QWORD**)</dt> </dl>                          | Attributo fusion flag mask.<br/>                                                                         |
| <span id="TAG_FLAG_PROCESSPARAM"></span><span id="tag_flag_processparam"></span><dl> <dt>**TAG \_ FLAG \_ PROCESSPARAM**</dt> <dt>(0xF \| **TAG \_ TYPE \_ QWORD**)</dt> </dl>                        | Attributo del flag del parametro del processo.<br/>                                                                       |
| <span id="TAG_FLAG_LUA"></span><span id="tag_flag_lua"></span><dl> <dt>**TAG \_ FLAG \_ LUA**</dt> <dt>(0x10 \| **TAG \_ TYPE \_ QWORD**)</dt> </dl>                                                  | Attributo del flag LUA.<br/>                                                                                 |
| <span id="TAG_FLAG_INSTALL"></span><span id="tag_flag_install"></span><dl> <dt>**TAG \_ INSTALLAZIONE \_ FLAG**</dt> <dt>(0X11 \| **TIPO DI TAG \_ \_ QWORD**)</dt> </dl>                                      | Installare l'attributo flag.<br/>                                                                             |



Le voci seguenti sono di tipo **TAG \_ TYPE \_ BINARY** (0x9000).



| Costante/valore                                                                                                                                                                                                                                                     | Descrizione                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span id="TAG_PATCH_BITS"></span><span id="tag_patch_bits"></span><dl> <dt>**TAG \_ PATCH \_ BITS**</dt> <dt>(0X2 \| **TIPO DI TAG \_ \_ BINARY**)</dt> </dl>              | Attributo patch file bits.<br/>                          |
| <span id="TAG_FILE_BITS"></span><span id="tag_file_bits"></span><dl> <dt>**TAG \_ BIT \_ DI FILE**</dt> <dt>(0X3 TIPO DI TAG \| **\_ \_ BINARY**)</dt> </dl>                 | Attributo bit del file.<br/>                                |
| <span id="TAG_EXE_ID"></span><span id="tag_exe_id"></span><dl> <dt>**TAG \_ EXE \_ ID**</dt> <dt>(0X4 \| **TIPO DI TAG \_ \_ BINARY**)</dt> </dl>                          | **Attributo GUID** di una voce eseguibile.<br/>          |
| <span id="TAG_DATA_BITS"></span><span id="tag_data_bits"></span><dl> <dt>**TAG \_ BIT \_ DI DATI**</dt> <dt>(0X5 TIPO DI TAG \| **\_ \_ BINARY**)</dt> </dl>                 | Attributo dei bit di dati.<br/>                                |
| <span id="TAG_MSI_PACKAGE_ID"></span><span id="tag_msi_package_id"></span><dl> <dt>**TAG \_ ID \_ \_ PACCHETTO MSI**</dt> <dt>(0X6 TIPO DI TAG \| **\_ \_ BINARY**)</dt> </dl> | Attributo dell'identificatore del pacchetto MSI di un pacchetto MSI.<br/> |
| <span id="TAG_DATABASE_ID"></span><span id="tag_database_id"></span><dl> <dt>**TAG \_ DATABASE \_ ID**</dt> <dt>(0X7 \| **TIPO DI TAG \_ \_ BINARY**)</dt> </dl>           | **Attributo GUID** di un database.<br/>                   |
| <span id="TAG_INDEX_BITS"></span><span id="tag_index_bits"></span><dl> <dt>**TAG \_ BIT \_ DI INDICE**</dt> <dt>(0X801 TIPO DI TAG \| **\_ \_ BINARY**)</dt> </dl>            | Attributo bit di indice.<br/>                               |



Le voci seguenti sono di tipo **TAG \_ TYPE \_ WORD** (0x3000).



| Costante/valore                                                                                                                                                                                                                                      | Descrizione                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| <span id="TAG_MATCH_MODE"></span><span id="tag_match_mode"></span><dl> <dt>**TAG \_ MODALITÀ \_ DI CORRISPONDENZA**</dt> <dt>(0x1 TAG DIGITARE \| **\_ \_ WORD**)</dt> </dl> | Attributo modalità di corrispondenza.<br/>                   |
| <span id="TAG_TAG"></span><span id="tag_tag"></span><dl> <dt>**TAG \_ TAG**</dt> <dt>(0x801 \| **TAG \_ TYPE \_ WORD**)</dt> </dl>                     | Voce TAG.<br/>                              |
| <span id="TAG_INDEX_TAG"></span><span id="tag_index_tag"></span><dl> <dt>**TAG \_ INDEX \_ TAG**</dt> <dt>(0X802 TAG TYPE \| **\_ \_ WORD**)</dt> </dl>  | Attributo TAG di indice per una voce di indice.<br/> |
| <span id="TAG_INDEX_KEY"></span><span id="tag_index_key"></span><dl> <dt>**TAG \_ INDEX \_ KEY**</dt> <dt>(0x803 \| **TAG TYPE \_ \_ WORD**)</dt> </dl>  | Attributo chiave di indice per una voce di indice.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Exposeenums2managed.h (includere Axextendenums.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi DI TAG](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




