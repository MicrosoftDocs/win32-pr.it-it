---
title: Classe ms-DS-Bindable-Object
description: Classe ausiliaria per rappresentare un oggetto associabile. Qualsiasi classe definita dall'utente che rappresenta un'entità che può essere utilizzata per eseguire il binding alla directory, ovvero un utente, deve includere questa classe ausiliaria.
ms.assetid: 181b3e2b-9442-4f11-9af7-4697491115f3
ms.tgt_platform: multiple
keywords:
- Schema di Active Directory della classe di oggetti ms-DS-Bindable
- Schema di Active Directory della classe msDS-BindableObject
topic_type:
- apiref
api_name:
- ms-DS-Bindable-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb69036ad9cd33b8f0a60f5356192acbea8dd71
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875069"
---
# <a name="ms-ds-bindable-object-class"></a>Classe ms-DS-Bindable-Object

Classe ausiliaria per rappresentare un oggetto associabile. Qualsiasi classe definita dall'utente che rappresenta un'entità che può essere utilizzata per eseguire il binding alla directory, ovvero un utente, deve includere questa classe ausiliaria.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | ms-DS-associabile-oggetto                |
| LDAP-Display-Name | msDS-BindableObject                  |
| Privilegio aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Schema-ID-GUID    | 89f4a69f-4416-6b49-821d-6e3c4a0ff802 |



## <a name="implementations"></a>Implementazioni

-   [**ADAM**](#adam-attributes)

## <a name="adam"></a>ADAM

-   [Attributes (Attributi)](#adam-attributes)



| Voce | Valore |
|-----------------------------|--------------------------------------------------------------|
| System-Only                 | Falso                                                        |
| Object-Category             | 3                                                            |
| Default-Object-Category     | \-                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.244                                       |
| Valore predefinito-nascondiglio        | 1                                                            |
| RDN-att-ID                  | \-                                                           |
| Sottoclasse di                 | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |
| Possibili superiori          | \-                                                           |
| Classi ausiliarie           | \-                                                           |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                 |
| Descrittore di sicurezza predefinito | \-                                                           |
| System-Flags                | 0x00000010                                                   |



## <a name="adam-attributes"></a>Attributi ADAM

Questa classe contiene gli attributi seguenti per ADAM:



| Attributo                                                                                      | Obbligatorio | Derivato da                                                                                 |
|------------------------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Account-scadenza**](a-accountexpires.md)                                                    | Falso     | **ms-DS-associabile-oggetto**                                                                    |
| [**Admin-Descrizione**](a-admindescription.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Attributi consentiti**](a-allowedattributes.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Password-ora non valida**](a-badpasswordtime.md)                                                 | Falso     | **ms-DS-associabile-oggetto**                                                                    |
| [**Numero di PWD non valido**](a-badpwdcount.md)                                                         | Falso     | **ms-DS-associabile-oggetto**                                                                    |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Nome canonico**](a-canonicalname.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Nome comune**](a-cn.md)                                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Creazione timestamp**](a-createtimestamp.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Descrizione**](a-description.md)                                                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Nome visualizzato**](a-displayname.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**DSA-firma**](a-dsasignature.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Da-entry**](a-fromentry.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Tipo di istanza**](a-instancetype.md)                                                        | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Viene eliminato**](a-isdeleted.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Is-member-of-DL**](a-memberof.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Ultimo accesso-timestamp**](a-lastlogontimestamp.md)                                           | Falso     | **ms-DS-associabile-oggetto**                                                                    |
| [**Tempo di blocco**](a-lockouttime.md)                                                          | Falso     | **ms-DS-associabile-oggetto**                                                                    |
| [**Oggetti gestiti**](a-managedobjects.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Mastered-by**](a-masteredby.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Modifica-timestamp**](a-modifytimestamp.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Disable-for-instances-BL**](a-msds-disableforinstancesbl.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-service-account-BL**](a-msds-serviceaccountbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-user-account-bloccato automaticamente**](a-ms-ds-useraccountautolocked.md)                        | Falso     | **ms-DS-associabile-oggetto**                                                                    |
| [**ms-DS-User-Account-Control-calcolato**](a-msds-user-account-control-computed.md)            | Falso     | **ms-DS-associabile-oggetto**                                                                    |
| [**ms-DS-user-account-disabilitato**](a-msds-useraccountdisabled.md)                              | Falso     | **ms-DS-associabile-oggetto**                                                                    |
| [**ms-DS-utente-dont-expire-password**](a-msds-userdontexpirepassword.md)                       | Falso     | **ms-DS-associabile-oggetto**                                                                    |
| [**ms-DS-utente-crittografato-testo-password-consentito**](a-ms-ds-userencryptedtextpasswordallowed.md) | Falso     | **ms-DS-associabile-oggetto**                                                                    |
| [**ms-DS-utente-password-scaduto**](a-msds-userpasswordexpired.md)                              | Falso     | **ms-DS-associabile-oggetto**                                                                    |
| [**ms-DS-utente-password-non obbligatorio**](a-ms-ds-userpasswordnotrequired.md)                    | Falso     | **ms-DS-associabile-oggetto**                                                                    |
| [**NT-pwd-cronologia**](a-ntpwdhistory.md)                                                       | Falso     | **ms-DS-associabile-oggetto**                                                                    |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                                       | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Categoria oggetto**](a-objectcategory.md)                                                    | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**Classe Object**](a-objectclass.md)                                                          | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**GUID oggetto**](a-objectguid.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Oggetto-SID**](a-objectsid.md)                                                              | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Versione oggetto**](a-objectversion.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Set di attributi parziali**](a-partialattributeset.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Possibili-inferiori**](a-possibleinferiors.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Pwd-ultimo set**](a-pwdlastset.md)                                                           | Falso     | **ms-DS-associabile-oggetto**                                                                    |
| [**Query-criteri-BL**](a-querypolicybl.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Reps-da**](a-repsfrom.md)                                                                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Da Reps a**](a-repsto.md)                                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Revisione**](a-revision.md)                                                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Riferimenti secondari**](a-subrefs.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Supplementare-credenziali**](a-supplementalcredentials.md)                                  | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Flag di sistema**](a-systemflags.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Gruppi di token**](a-tokengroups.md)                                                          | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Unicode-pwd**](a-unicodepwd.md)                                                            | Falso     | **ms-DS-associabile-oggetto**                                                                    |
| [**USN-modificato**](a-usnchanged.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN creato**](a-usncreated.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-tra siti**](a-usnintersite.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-origine**](a-usnsource.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**WBEM-percorso**](a-wbempath.md)                                                                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Oggetti noti**](a-wellknownobjects.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Quando-modificato**](a-whenchanged.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Data di creazione**](a-whencreated.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**WWW-pagina-altro**](a-url.md)                                                                | Falso     | [**In alto**](c-top.md)<br/>                                                              |



 

 





