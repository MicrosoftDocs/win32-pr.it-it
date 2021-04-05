---
description: In generale, ogni oggetto Active Directory viene mappato esattamente a un'istanza di WMI.
ms.assetid: c6c7f3c3-7174-4278-bf40-d99ed8bd0c8d
ms.tgt_platform: multiple
title: Mapping di istanze di Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51eaec7b2c6ef121d0f65df375e1bb0fce32cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057862"
---
# <a name="mapping-active-directory-instances"></a>Mapping di istanze di Active Directory

In generale, ogni oggetto Active Directory viene mappato esattamente a un'istanza di WMI. La classe WMI corrispondente all'istanza WMI corrisponde alla classe fornita dal provider di classi dalla classe Active Directory corrispondente. La proprietà chiave **ADSIPath** di ogni istanza viene compilata con il percorso ADSI dell'oggetto.

Le sezioni seguenti sono illustrate in questo argomento:

-   [Mapping di spazi dei nomi](#mapping-namespaces)
-   [Mapping di valori di attributo](#mapping-attribute-values)
-   [Mapping di associazioni di istanze](#mapping-instance-associations)

> [!Note]  
> Per ulteriori informazioni sul supporto e l'installazione di questo componente in un sistema operativo specifico, vedere la pagina relativa alla [disponibilità del sistema operativo dei componenti WMI](operating-system-availability-of-wmi-components.md).

 

## <a name="mapping-namespaces"></a>Mapping di spazi dei nomi

Ogni spazio dei nomi in ADSI mappa uno-a-uno agli spazi dei nomi nello \\ \\ spazio dei nomi della directory radice WMI. Il nome dello spazio dei nomi WMI corrisponde al valore **ProgID** del provider di servizi directory che fornisce lo spazio dei nomi. In particolare, Active Directory esegue il mapping allo \\ spazio dei nomi LDAP nello \\ \\ spazio dei nomi della directory radice. WMI crea lo \\ spazio dei nomi LDAP come parte del processo di registrazione del provider di classi.

## <a name="mapping-attribute-values"></a>Mapping di valori di attributo

Nella tabella seguente viene elencato il mapping tra ogni attributo di un oggetto Active Directory e una proprietà WMI.



| Sintassi Active Directory | Tipo di dati WMI                                 | Valore della proprietà WMI                                                        |
|-------------------------|-----------------------------------------------|---------------------------------------------------------------------------|
| Access-Point            | **\_stringa CIM**                               | Mappato dal valore della stringa.                                      |
| Boolean                 | **\_valore booleano CIM**                              | Mappato direttamente al valore booleano appropriato.                         |
| Stringa senza distinzione tra maiuscole e minuscole | **\_stringa CIM**                               | Mappato dal valore della stringa.                                      |
| Stringa distinzione tra maiuscole e minuscole   | **\_stringa CIM**                               | Mappato dal valore della stringa.                                      |
| Nome distinto      | **\_stringa CIM**                               | Mappato dal valore della stringa.                                      |
| DN-Binary               | Oggetto incorporato della classe **DN \_ con \_ Binary** | Mappato a istanze del **DN \_ con classe \_ String** .                    |
| DN-String               | Oggetto incorporato della classe **DN \_ con \_ stringa** | Mappato a istanze del **DN \_ con classe \_ String** .                    |
| Enumerazione             | **\_SINT32 CIM**                               | Mappato direttamente al valore intero.                                     |
| IA5-String              | **\_stringa CIM**                               | Mappato dal valore della stringa.                                      |
| Integer                 | **\_SINT32 CIM**                               | Mappato direttamente al valore intero.                                     |
| Descrittore di sicurezza NT  | Oggetto incorporato della classe **Uint8Array**       | Mappato a istanze della classe **Uint8Array** .                          |
| Stringa numerica          | **\_stringa CIM**                               | Mappato dal valore della stringa.                                      |
| ID oggetto               | **\_stringa CIM**                               | Mappato dalla rappresentazione di stringa dell'OID; ad esempio, "1.3.3.4". |
| Stringa ottetto            | Oggetto incorporato della classe **Uint8Array**       | Mappato a istanze della classe **Uint8Array** .                          |
| O nome                 | **\_stringa CIM**                               | Mappato dal valore della stringa.                                      |
| Presentation-Address    | **\_stringa CIM**                               | Mappato dal valore della stringa.                                      |
| Stringa del case di stampa       | **\_stringa CIM**                               | Mappato dal valore della stringa.                                      |
| Collegamento replica            | Oggetto incorporato della classe **Uint8Array**       | Mappato a istanze della classe **Uint8Array** .                          |
| SID                     | Oggetto incorporato della classe **Uint8Array**       | Mappato a istanze della classe **Uint8Array** .                          |
| Tempo                    | **\_DateTime CIM**                             | Convertito nella rappresentazione di \_ DateTime CIM e mappato.                 |
| Non definito               | N/D                                           | N/D                                                                       |
| Stringa Unicode          | **\_stringa CIM**                               | Mappato dal valore della stringa.                                      |
| Ora codificata UTC          | **\_DateTime CIM**                             | Convertito nella rappresentazione di \_ DateTime CIM e mappato.                 |



 

Per altre informazioni su **Uint8Array** e **DN \_ con \_ Binary**, vedere [mapping degli attributi](mapping-active-directory-classes.md).

## <a name="mapping-instance-associations"></a>Mapping di associazioni di istanze

Il provider di servizi directory esegue il mapping delle diverse relazioni tra contenitori in Active Directory usando le istanze della classe di [**\_ \_ \_ contenimento dell'istanza di DS LDAP**](/previous-versions/windows/desktop/dsprov/ds-ldap-instance-containment) .

 

 
