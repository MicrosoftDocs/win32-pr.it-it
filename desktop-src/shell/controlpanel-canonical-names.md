---
description: A partire da Windows Vista, agli elementi del pannello di controllo inclusi in Windows viene assegnato un nome canonico che può essere utilizzato in una chiamata API o un'istruzione della riga di comando per avviare l'elemento a livello di codice.
ms.assetid: A02DFC9F-646D-40d8-901C-7239A820DE2C
title: Nomi canonici degli elementi del pannello di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a55fc360b0d3db0f85a057977d1898c59d09d5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966525"
---
# <a name="canonical-names-of-control-panel-items"></a>Nomi canonici degli elementi del pannello di controllo

A partire da Windows Vista, agli elementi del pannello di controllo inclusi in Windows viene assegnato un nome canonico che può essere utilizzato in una [chiamata API o un'istruzione della riga di comando](executing-control-panel-items.md) per avviare l'elemento a livello di codice. A partire da Windows 7 e Windows Server 2008 R2, i nomi canonici possono essere usati in un criterio di gruppo per nascondere elementi specifici del pannello di controllo. Questo argomento fornisce informazioni dettagliate per ogni elemento del pannello di controllo: nome canonico, GUID, nome del modulo e versioni del sistema operativo che riconoscono il nome canonico.

> [!Note]  
> I nomi canonici per gli elementi del pannello di controllo non sono supportati prima di Windows Vista.

 

-   [Nomi canonici del pannello di controllo](#control-panel-canonical-names)
-   [Nomi canonici del pannello di controllo deprecati](#deprecated-control-panel-canonical-names)
-   [Uso di nomi canonici in Criteri di gruppo](#using-canonical-names-in-local-group-policy)
-   [Osservazioni:](#remarks)

## <a name="control-panel-canonical-names"></a>Nomi canonici del pannello di controllo

Punti da ricordare quando si utilizzano questi valori:

-   Per definizione, i nomi canonici non cambiano in base alla lingua del sistema; sono sempre in inglese, anche se la lingua del sistema non lo è.
-   Non tutti gli elementi del pannello di controllo sono presenti in tutte le varietà di finestre.
-   Alcuni elementi del pannello di controllo vengono visualizzati solo se viene rilevato l'hardware corretto nel sistema.
-   Anche le terze parti possono aggiungere elementi del pannello di controllo. I nomi canonici elencati di seguito sono solo per gli elementi del pannello di controllo inclusi in Windows.

Di seguito sono riportati gli elementi del pannello di controllo disponibili in Windows 8.1:

-   [Centro notifiche](#action-center)
-   [Strumenti di amministrazione](#administrative-tools)
-   [AutoPlay](#autoplay)
-   [Dispositivi biometrici](#biometric-devices)
-   [Crittografia unità BitLocker](#bitlocker-drive-encryption)
-   [Gestione dei colori](#color-management)
-   [Gestione credenziali](#credential-manager)
-   [Data e ora](#date-and-time)
-   [Programmi predefiniti](#default-programs)
-   [Gestione dispositivi](#device-manager)
-   [Dispositivi e stampanti](#devices-and-printers)
-   [Schermo](#display)
-   [Centro accesso facilitato](#ease-of-access-center)
-   [Protezione per la famiglia](#family-safety)
-   [Cronologia file](#file-history)
-   [Opzioni cartella](#folder-options)
-   [Tipi di carattere](#fonts)
-   [Gruppo Home](#homegroup)
-   [Opzioni di indicizzazione](#indexing-options)
-   [Infrarossi](#infrared)
-   [Opzioni Internet](#internet-options)
-   [Iniziatore iSCSI](#iscsi-initiator)
-   [Server iSNS](#isns-server)
-   [Tastiera](#keyboard)
-   [Impostazioni percorso](#location-settings)
-   [Mouse](#mouse)
-   [MPIOConfiguration](#mpioconfiguration)
-   [Centro connessioni di rete e condivisione](#network-and-sharing-center)
-   [Icone dell'area di notifica](#notification-area-icons)
-   [Penna e tocco](#pen-and-touch)
-   [Personalizzazione](#personalization)
-   [Telefono e modem](#phone-and-modem)
-   [Opzioni risparmio energia](#power-options)
-   [Programmi e funzionalità](#programs-and-features)
-   [Ripristino](#recovery)
-   [Area](#region)
-   [Connessioni RemoteApp e desktop](#remoteapp-and-desktop-connections)
-   [Suoni](#sound)
-   [Riconoscimento vocale](#speech-recognition)
-   [Spazi di archiviazione](#storage-spaces)
-   [Centro sincronizzazione](#sync-center)
-   [Sistema](#system)
-   [Impostazioni Tablet PC](#tablet-pc-settings)
-   [Barra delle applicazioni e navigazione](#taskbar-and-navigation)
-   [Risoluzione dei problemi](#troubleshooting)
-   [TSAppInstall](#tsappinstall)
-   [Account utente](#user-accounts)
-   [Windows Anytime Upgrade](#windows-anytime-upgrade)
-   [Windows Defender](#windows-defender)
-   [Windows Firewall](#windows-firewall)
-   [Centro PC portatile Windows](#windows-mobility-center)
-   [Windows To Go](#windows-to-go)
-   [Windows Update](#windows-update)
-   [Cartelle di lavoro](#work-folders)

### <a name="action-center"></a>Centro notifiche

-   **Nome canonico**: Microsoft. ActionCenter
-   **GUID**: {BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}
-   **Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\ActionCenterCPL.dll,-1
-   **Pagine**

    | Nome pagina           | Opens                      |
    |---------------------|----------------------------|
    | MaintenanceSettings | Manutenzione automatica      |
    | pageProblems        | Segnalazioni di problemi            |
    | pageReliabilityView | Monitoraggio affidabilità        |
    | pageResponseArchive | Messaggi archiviati          |
    | pageSettings        | Impostazioni segnalazione problemi |

    

     

### <a name="administrative-tools"></a>Strumenti di amministrazione

-   **Nome canonico**: Microsoft. AdministrativeTools
-   **GUID**: {D20EA4E1-3957-11D2-A40B-0C5020524153}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\shell32.dll,-22982

### <a name="autoplay"></a>AutoPlay

-   **Nome canonico**: Microsoft. AutoPlay
-   **GUID**: {9C60DE1E-E5FC-40F4-A487-460851A8D915}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\autoplay.dll,-1

### <a name="biometric-devices"></a>Dispositivi biometrici

-   **Nome canonico**: Microsoft. BiometricDevices
-   **GUID**: {0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}
-   **Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\biocpl.dll,-1

### <a name="bitlocker-drive-encryption"></a>Crittografia unità BitLocker

-   **Nome canonico**: Microsoft. BitLockerDriveEncryption
-   **GUID**: {D9EF8727-CaC2-4E60-809E-86F80A666C91}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\fvecpl.dll,-1

### <a name="color-management"></a>Gestione dei colori

-   **Nome canonico**: Microsoft. ColorManagement
-   **GUID**: {B2C761C6-29BC-4F19-9251-E6195265BAF1}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\colorcpl.exe,-6

### <a name="credential-manager"></a>Gestione credenziali

-   **Nome canonico**: Microsoft. CredentialManager
-   **GUID**: {1206F5F1-0569-412C-8FEC-3204630DFB70}
-   **Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\Vault.dll,-1
-   **Pagine**

    | Nome pagina                   | Opens               |
    |-----------------------------|---------------------|
    | ? SelectedVault = CredmanVault | Credenziali di Windows |

    

     

### <a name="date-and-time"></a>Data e ora

-   **Nome canonico**: Microsoft. DateAndTime
-   **GUID**: {E2E7934B-DCE5-43C4-9576-7FE4F75E7480}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\timedate.cpl,-51
-   **Pagine**

    | Nome pagina | Opens             |
    |-----------|-------------------|
    | 1         | Orologi aggiuntivi |

    

     

### <a name="default-programs"></a>Programmi predefiniti

-   **Nome canonico**: Microsoft. DefaultPrograms
-   **GUID**: {17cd9488-1228-4b2f-88ce-4298e93e0966}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\sud.dll,-1
-   **Pagine**

    | Nome pagina          | Opens                |
    |--------------------|----------------------|
    | pageDefaultProgram | Imposta programmi predefiniti |
    | pageFileAssoc      | Imposta associazioni     |

    

     

### <a name="device-manager"></a>Gestione dispositivi

-   **Nome canonico**: Microsoft. devicemanager
-   **GUID**: {74246bfc-4c96-11D0-abef-0020af6b0b7a}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\devmgr.dll,-4

### <a name="devices-and-printers"></a>Dispositivi e stampanti

-   **Nome canonico**: Microsoft. DevicesAndPrinters
-   **GUID**: {A8A91A66-3A7D-4424-8D24-04E180695C7A}
-   **Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\DeviceCenter.dll,-1000

### <a name="display"></a>Visualizza

-   **Nome canonico**: Microsoft. display
-   **GUID**: {C555438B-3C23-4769-A71F-B6D3D9B6053A}
-   **Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\Display.dll,-1
-   **Pagine**

    | Nome pagina | Opens             |
    |-----------|-------------------|
    | Impostazioni  | Risoluzione dello schermo |

    

     

### <a name="ease-of-access-center"></a>Centro accesso facilitato

-   **Nome canonico**: Microsoft. EaseOfAccessCenter
-   **GUID**: {D555645E-D4F8-4c29-A827-D93C859C4F2A}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\accessibilitycpl.dll,-10
-   **Pagine**

    | Nome pagina               | Opens                                                               |
    |-------------------------|---------------------------------------------------------------------|
    | pageEasierToClick       | Semplifica l'uso del mouse                                        |
    | pageEasierToSee         | Semplifica la visualizzazione del computer                                     |
    | pageEasierWithSounds    | Usare il testo o le alternative visive per i suoni                          |
    | pageFilterKeysSettings  | Configurare chiavi di filtro                                                  |
    | pageKeyboardEasierToUse | Semplifica l'uso della tastiera                                     |
    | pageNoMouseOrKeyboard   | Utilizzare il computer senza mouse o tastiera                        |
    | pageNoVisual            | Usare il computer senza visualizzazione                                  |
    | pageQuestionsCognitive  | Ottenere consigli per semplificare l'uso del computer (cognitive) |
    | pageQuestionsEyesight   | Ottenere consigli per semplificare l'uso del computer (vista)  |

    

     

### <a name="family-safety"></a>Protezione per la famiglia

-   **Nome canonico**: Microsoft. parentalcontrols
-   **GUID**: {96AE8D84-A250-4520-95A5-A47A7E3C548B}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\wpccpl.dll,-100
-   **Pagine**

    | Nome pagina   | Opens                                  |
    |-------------|----------------------------------------|
    | pageUserHub | Scegliere un utente e configurare la sicurezza delle famiglie |

    

     

### <a name="file-history"></a>Cronologia file

-   **Nome canonico**: Microsoft. filehistory
-   **GUID**: {F6B6E965-E9B2-444B-9286-10C9152EDBC5}
-   **Sistema operativo supportato**: Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\fhcpl.dll,-52
-   La cronologia file include una versione più recente dell'elemento di backup e ripristino, ma il nome canonico dell'elemento precedente non viene rimappato alla cronologia file.

### <a name="folder-options"></a>Opzioni cartella

-   **Nome canonico**: Microsoft. FolderOptions
-   **GUID**: {6DFD7C5C-2451-11D3-A299-00C04F8EF6AF}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\shell32.dll,-22985

### <a name="fonts"></a>Tipi di carattere

-   **Nome canonico**: Microsoft. Fonts
-   **GUID**: {93412589-74D4-4E4E-AD0E-E0CB621440FD}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\FontExt.dll,-8007

### <a name="homegroup"></a>Gruppo Home

-   **Nome canonico**: Microsoft. Gruppo Home
-   **GUID**: {67CA7650-96E6-4fdd-BB43-A8E774F73A57}
-   **Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\hgcpl.dll,-1

### <a name="indexing-options"></a>Opzioni di indicizzazione

-   **Nome canonico**: Microsoft. IndexingOptions
-   **GUID**: {87D66A43-7B11-4A28-9811-C86EE395ACF7}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\srchadmin.dll,-601

### <a name="infrared"></a>Infrarossi

-   **Nome canonico**: Microsoft. Infrared
-   **GUID**: {A0275511-0E86-4ECA-97C2-ECD8F1221D08}
-   **Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\irprops.cpl,-1

### <a name="internet-options"></a>Opzioni Internet

-   **Nome canonico**: Microsoft. InternetOptions
-   **GUID**: {A3DD4F92-658A-410f-84FD-6FBBBEF2FFFE}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @C: \\ Windows \\ system32 \\inetcpl.cpl,-4312
-   **Pagine**

    | Nome pagina | Opens       |
    |-----------|-------------|
    | 1         | Sicurezza    |
    | 2         | Privacy     |
    | 3         | Content     |
    | 4         | Connessioni |
    | 5         | Programmi    |
    | 6         | Avanzato    |

    

     

### <a name="iscsi-initiator"></a>Iniziatore iSCSI

-   **Nome canonico**: Microsoft. iSCSIInitiator
-   **GUID**: {A304259D-52B8-4526-8B1A-A1D6CECC8243}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\iscsicpl.dll,-5001

### <a name="isns-server"></a>Server iSNS

-   **Nome canonico**: Microsoft. iSNSServer
-   **GUID**: {0D2A3442-5181-4E3A-9BD4-83BD10AF3D76}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\isnssrv.dll,-5005
-   Questo elemento del pannello di controllo verrà visualizzato solo nelle versioni server di Windows.

### <a name="keyboard"></a>Tastiera

-   **Nome canonico**: Microsoft. Keyboard
-   **GUID**: {725BE8F7-668E-4c7b-8F90-46BDB0936430}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\main.cpl,-102

### <a name="location-settings"></a>Impostazioni percorso

-   **Nome canonico**: Microsoft. LocationSettings
-   **GUID**: {E9950154-C418-419e-A90A-20C5287AE24B}
-   **Sistema operativo supportato**: Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\SensorsCpl.dll,-1

### <a name="mouse"></a>Mouse

-   **Nome canonico**: Microsoft. mouse
-   **GUID**: {6C8EEC18-8D75-41B2-A177-8831D59D2D50}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\main.cpl,-100
-   **Pagine**

    | Nome pagina | Opens           |
    |-----------|-----------------|
    | 1         | Pointers        |
    | 2         | Opzioni puntatore |
    | 3         | Selettore circolare           |
    | 4         | Hardware        |

    

     

### <a name="mpioconfiguration"></a>MPIOConfiguration

-   **Nome canonico**: Microsoft. MPIOConfiguration
-   **GUID**: {AB3BE6AA-7561-4838-ab77-ACF8427DF426}
-   **Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\mpiocpl.dll,-1000
-   Questo elemento del pannello di controllo verrà visualizzato solo nelle versioni server di Windows.

### <a name="network-and-sharing-center"></a>Centro connessioni di rete e condivisione

-   **Nome canonico**: Microsoft. NetworkAndSharingCenter
-   **GUID**: {8E908FC9-Becc-40f6-915B-F4CA0E70D03D}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\netcenter.dll,-1
-   **Pagine**

    | Nome pagina  | Opens                     |
    |------------|---------------------------|
    | Avanzato   | Impostazioni di condivisione avanzate |
    | ShareMedia | Opzioni di streaming multimediale   |

    

     

### <a name="notification-area-icons"></a>Icone dell'area di notifica

-   **Nome canonico**: Microsoft. NotificationAreaIcons
-   **GUID**: {05d7b0f4-2121-4eff-bf6b-ed3f69b894d9}
-   **Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\taskbarcpl.dll,-1

### <a name="pen-and-touch"></a>Penna e tocco

-   **Nome canonico**: Microsoft. PenAndTouch
-   **GUID**: {F82DF8F7-8B9F-442E-A48C-818EA735FF9B}
-   **Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\tabletpc.cpl,-10103
-   **Pagine**

    | Nome pagina | Opens       |
    |-----------|-------------|
    | 1         | I gesti rapidi      |
    | 2         | Scrittura a mano |

    

     

### <a name="personalization"></a>Personalization

-   **Nome canonico**: Microsoft. personalizzazione
-   **GUID**: {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\themecpl.dll,-1
-   **Pagine**

    | Nome pagina        | Opens                |
    |------------------|----------------------|
    | pageColorization | Colore e aspetto |
    | pageWallpaper    | Sfondo del desktop   |

    

     

### <a name="phone-and-modem"></a>Telefono e modem

-   **Nome canonico**: Microsoft. PhoneAndModem
-   **GUID**: {40419485-c444-4567-851A-2DD7BFA1684D}
-   **Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\telephon.cpl,-1
-   La finestra avviata da questo valore è intitolata "Information location" nelle versioni di Windows precedenti a Windows 8. L'interfaccia utente dell'elemento è notevolmente cambiata a partire da Windows 8.

### <a name="power-options"></a>Opzioni risparmio energia

-   **Nome canonico**: Microsoft. PowerOptions
-   **GUID**: {025A5937-A6BE-4686-A844-36FE4BEC8B6D}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\powercpl.dll,-1
-   **Pagine**

    | Nome pagina          | Opens              |
    |--------------------|--------------------|
    | pageGlobalSettings | Impostazioni sistema    |
    | pagePlanSettings   | Modificare le impostazioni del piano |

    

     

### <a name="programs-and-features"></a>Programmi e funzionalità

-   **Nome canonico**: Microsoft. ProgramsAndFeatures
-   **GUID**: {7b81be6a-ce2b-4676-A29E-eb907a5126c5}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\appwiz.cpl,-159
-   **Pagine**

    | Nome pagina                                | Opens             |
    |------------------------------------------|-------------------|
    | ::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD} | Aggiornamenti installati |

    

     

### <a name="recovery"></a>Ripristino

-   **Nome canonico**: Microsoft. Recovery
-   **GUID**: {9FE63AFD-59CF-4419-9775-ABCC3849F861}
-   **Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\recovery.dll,-101

### <a name="region"></a>Region

-   **Nome canonico**: Microsoft. RegionAndLanguage
-   **GUID**: {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}
-   **Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\intl.cpl,-1
-   L'elemento Region e Language trovato in Windows 7 è stato suddiviso a partire da Windows 8. Microsoft. RegionAndLanguage ora avvia l'elemento Region. Per avviare l'elemento della lingua, utilizzare [Microsoft. Language](#location-settings).
-   **Pagine**

    | Nome pagina | Opens          |
    |-----------|----------------|
    | 1         | Location       |
    | 2         | Amministrativo |

    

     

### <a name="remoteapp-and-desktop-connections"></a>Connessioni RemoteApp e desktop

-   **Nome canonico**: Microsoft. RemoteAppAndDesktopConnections
-   **GUID**: {241D7C96-F8BF-4F85-B01F-E2B043341A4B}
-   **Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\tsworkspace.dll,-15300

### <a name="sound"></a>Suoni

-   **Nome canonico**: Microsoft. Sound
-   **GUID**: {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}
-   **Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\mmsys.cpl,-300

### <a name="speech-recognition"></a>Riconoscimento vocale

-   **Nome canonico**: Microsoft. sintesi vocale
-   **GUID**: {58E3C745-D971-4081-9034-86E34B30836A}
-   **Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ System32 \\ Speech \\ SpeechUX \\speechuxcpl.dll,-1

### <a name="storage-spaces"></a>Spazi di archiviazione

-   **Nome canonico**: Microsoft. StorageSpaces
-   **GUID**: {F942C606-0914-47AB-BE56-1321B8035096}
-   **Sistema operativo supportato**: Windows 8, Windows 8.1
-   **Nome del modulo**: @C: \\ Windows \\ system32 \\SpaceControl.dll,-1

### <a name="sync-center"></a>Centro sincronizzazione

-   **Nome canonico**: Microsoft. synccenter
-   **GUID**: {9C73F5E5-7AE7-4E32-A8E8-8D23B85255BF}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\SyncCenter.dll,-3000

### <a name="system"></a>Sistema

-   **Nome canonico**: Microsoft.System
-   **GUID**: {BB06C0E4-D293-4f75-8A90-CB05B6477EEE}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\systemcpl.dll,-1

### <a name="tablet-pc-settings"></a>Impostazioni Tablet PC

-   **Nome canonico**: Microsoft. TabletPCSettings
-   **GUID**: {80F3F1D5-Feca-45F3-BC32-752C152E456E}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\tabletpc.cpl,-10100

### <a name="taskbar-and-navigation"></a>Barra delle applicazioni e navigazione

-   **Nome canonico**: Microsoft. Taskbar
-   **GUID**: {0DF44EAA-FF21-4412-828E-260A8728E7F1}
-   **Sistema operativo supportato**: Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\shell32.dll,-32517

### <a name="troubleshooting"></a>Risoluzione dei problemi

-   **Nome canonico**: Microsoft. Troubleshooting
-   **GUID**: {C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}
-   **Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\DiagCpl.dll,-1
-   **Pagine**

    | Nome pagina   | Opens   |
    |-------------|---------|
    | HistoryPage | Cronologia |

    

     

### <a name="tsappinstall"></a>TSAppInstall

-   **Nome canonico**: Microsoft. TSAppInstall
-   **GUID**: {BAA884F4-3432-48b8-AA72-9BF20EEF31D5}
-   **Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\tsappinstall.exe,-2001

### <a name="user-accounts"></a>Account utente

-   **Nome canonico**: Microsoft. UserAccounts
-   **GUID**: {60632754-C523-4b62-B45C-4172da012619}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\usercpl.dll,-1

### <a name="windows-anytime-upgrade"></a>Windows Anytime Upgrade

-   **Nome canonico**: Microsoft. WindowsAnytimeUpgrade
-   **GUID**: {BE122A0E-4503-11da-8BDE-F66BAD1E3F3A}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @ $ (resourceString. \_ \_Percorso sys mod \_ ),-1

### <a name="windows-defender"></a>Windows Defender

-   **Nome canonico**: Microsoft. Windowsdefender
-   **GUID**: {D8559EB9-20C0-410e-Beda-7ED416AECC2A}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% ProgramFiles% \\ Windows Defender \\MsMpRes.dll,-104

### <a name="windows-firewall"></a>Windows Firewall

-   **Nome canonico**: Microsoft. WindowsFirewall
-   **GUID**: {4026492F-2F69-46B8-B9BF-5654FC07E423}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @C: \\ Windows \\ system32 \\FirewallControlPanel.dll,-12122
-   **Pagine**

    | Nome pagina         | Opens        |
    |-------------------|--------------|
    | pageConfigureApps | App consentite |

    

     

### <a name="windows-mobility-center"></a>Centro PC portatile Windows

-   **Nome canonico**: Microsoft. MobilityCenter
-   **GUID**: {5ea4f148-308C-46d7-98a9-49041b1dd468}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\mblctr.exe,-1002

### <a name="windows-to-go"></a>Windows To Go

-   **Nome canonico**: Microsoft. PortableWorkspaceCreator
-   **GUID**: {8E0C279D-0BD1-43C3-9EBD-31C3DC5B8A77}
-   **Sistema operativo supportato**: Windows 8, Windows 8.1
-   **Nome del modulo**: @% systemroot% \\ system32 \\pwcreator.exe,-151

### <a name="windows-update"></a>Windows Update

-   **Nome canonico**: Microsoft. windowsupdate
-   **GUID**: {36eef7db-88ad-4E81-ad49-0e313f0c35f8}
-   **Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome modulo**: @% systemroot% \\ system32 \\wucltux.dll,-1
-   **Pagine**

    | Nome pagina         | Opens               |
    |-------------------|---------------------|
    | pageSettings      | Cambia impostazioni     |
    | pageUpdateHistory | Visualizza cronologia aggiornamenti |

    

     

### <a name="work-folders"></a>Cartelle di lavoro

-   **Nome canonico**: Microsoft. cartellelavoro
-   **GUID**: {ECDB0924-4208-451E-8EE0-373C0956DE16}
-   **Sistema operativo supportato**: Windows 8.1
-   **Nome del modulo**: @C: \\ Windows \\ system32 \\WorkfoldersControl.dll,-1

## <a name="deprecated-control-panel-canonical-names"></a>Nomi canonici del pannello di controllo deprecati

Di seguito sono riportati nomi canonici che non sono più in uso a partire da Windows 8.1 o versione successiva. Alcune sono state rimosse completamente. Altre sono state rimappate in queste situazioni:

-   Un elemento del pannello di controllo è stato rinominato. All'elemento rinominato viene assegnato un nuovo nome canonico ma viene mantenuto lo stesso GUID. In questo caso, il vecchio nome canonico avvia l'elemento del pannello di controllo rinominato. Tenere presente che l'elemento avviato potrebbe non utilizzare la stessa interfaccia utente della versione precedente di tale elemento.
-   La funzionalità di uno o più elementi del pannello di controllo viene spostata o consolidata in un nuovo elemento. In questo caso, il nome canonico precedente esegue il mapping al nuovo elemento del pannello di controllo più appropriato.

> [!Note]  
> Sono disponibili nuovi mapping per la compatibilità con le versioni precedenti. Non usare valori deprecati nel nuovo codice.

 



| Nome canonico deprecato                                   | Elemento del pannello di controllo                | GUID                                   | Note                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Microsoft. AddHardware                                       | Aggiungi hardware                      | {7A979262-40CE-46ff-AEEE-7884AC3B6136} | Esegue il mapping a [Microsoft. DevicesAndPrinters](#devices-and-printers) a partire da Windows 7.                                                                                                                                                                                                                                                                            |
| Microsoft. AudioDevicesAndSoundThemes                        | Suoni                             | {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D} | Esegue il mapping a [Microsoft. Sound](#sound) a partire da Windows 7.                                                                                                                                                                                                                                                                                                        |
| Microsoft. BackupAndRestoreCenter/Microsoft. BackupAndRestore | Centro di backup e ripristino         | {B98A2BEA-7D42-4558-8BD1-832F41BAC6FD} | Microsoft. BackupAndRestoreCenter esegue il mapping a Microsoft. BackupAndRestore in Windows 7. Entrambi vengono rimossi a partire da Windows 8. in alternativa, utilizzare [Microsoft. filehistory](#file-history) .                                                                                                                                                                                   |
| Microsoft. CardSpace                                         | Windows CardSpace                 | {78CB147A-98EA-4AA6-B0DF-C8681F69341C} | Rimosso a partire da Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft. DesktopGadgets                                    | Gadget desktop                   | {37efd44d-ef8d-41b1-940d-96973a50e9e0} | Rimosso a partire da Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft. GetProgramsOnline                                 | Windows Marketplace               | {3e7efb4c-faf1-453d-89eb-56026875ef90} | Rimosso a partire da Windows 7.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft. InfraredOptions                                   | Infrarossi                          | {A0275511-0E86-4ECA-97C2-ECD8F1221D08} | Esegue il mapping a [Microsoft. Infrared](#infrared) a partire da Windows 7.                                                                                                                                                                                                                                                                                                  |
| Microsoft. Language                                          | Linguaggio                          | {BF782CC9-5A52-4A17-806C-2A894FFEEAC5} | Rimosso a partire da Windows 10, versione 1803                                                                                                                                                                                                                                                                                                                    |
| Microsoft. LocationAndOtherSensors                           | Posizione e altri sensori        | {E9950154-C418-419e-A90A-20C5287AE24B} | Esegue il mapping a [Microsoft. LocationSettings](#infrared) a partire da Windows 8.                                                                                                                                                                                                                                                                                          |
| Microsoft. PenAndInputDevices                                | Dispositivi di input e penna             | {F82DF8F7-8B9F-442E-A48C-818EA735FF9B} | Esegue il mapping a [Microsoft. PenAndTouch](#pen-and-touch) a partire da Windows 7.                                                                                                                                                                                                                                                                                          |
| Microsoft. PeopleNearMe                                      | Persone nelle vicinanze                    | {5224F545-A443-4859-BA23-7B5A95BDC8EF} | Rimosso a partire da Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft. PerformanceInformationAndTools                    | Strumenti e informazioni sulle prestazioni | {78F3955E-3B90-4184-BD14-5397C15F1EFC} | Rimosso a partire da Windows 8.1.                                                                                                                                                                                                                                                                                                                                |
| Microsoft. PhoneAndModemOptions                              | Telefono e modem                   | {40419485-C444-4567-851A-2DD7BFA1684D} | Esegue il mapping a [Microsoft. PhoneAndModem](#phone-and-modem) a partire da Windows 7.                                                                                                                                                                                                                                                                                      |
| Microsoft. stampanti                                          | Stampanti                          | {2227A280-3AEA-1069-A2DE-08002B30309D} | Esegue il mapping a [Microsoft. DevicesAndPrinters](#devices-and-printers) a partire da Windows 7.                                                                                                                                                                                                                                                                            |
| Microsoft. ProblemReportsAndSolutions                        | Segnalazioni di problemi e soluzioni     | {FCFEECAE-EE1B-4849-AE50-685DCF7717EC} | Esegue il mapping a [Microsoft. ActionCenter](#action-center) a partire da Windows 7.                                                                                                                                                                                                                                                                                         |
| Microsoft. RegionalAndLanguageOptions                        | Opzioni internazionali e della lingua     | {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0} | Esegue il mapping a [Microsoft. RegionAndLanguage](#region) a partire da Windows 7. Si noti che a partire da Windows 8, Region e Language sono stati assegnati a ogni elemento del pannello di controllo. Microsoft. RegionalAndLanguageOptions e Microsoft. RegionAndLanguage Attualmente aprono l'elemento Region. Per accedere all'elemento del linguaggio, è necessario utilizzare [Microsoft. Language](#location-settings) . |
| Microsoft. SecurityCenter                                    | Centro sicurezza Windows           | {087DA31B-0DD3-4537-8E23-64A18591F88B} | Esegue il mapping a [Microsoft. ActionCenter](#action-center) a partire da Windows 7.                                                                                                                                                                                                                                                                                         |
| Microsoft. SpeechRecognitionOptions                          | Opzioni di riconoscimento vocale        | {58E3C745-D971-4081-9034-86E34B30836A} | Esegue il mapping a [Microsoft. sintesi vocale](#speech-recognition) a partire da Windows 7.                                                                                                                                                                                                                                                                               |
| Microsoft. TaskbarAndStartMenu                               | Barra delle applicazioni e menu Start            | {0DF44EAA-FF21-4412-828E-260A8728E7F1} | Esegue il mapping a [Microsoft. Taskbar](#speech-recognition) a partire da Windows 8.                                                                                                                                                                                                                                                                                         |
| Microsoft. WelcomeCenter                                     | Centro di benvenuto                    | {CB1B7F8C-C50A-4176-B604-9E24DEE8D4D1} | Esegue il mapping a Microsoft. GettingStarted in Windows 7. Avvia il pannello di controllo home page a partire da Windows 8.                                                                                                                                                                                                                                                      |
| Microsoft. WindowsSidebarProperties                          | Proprietà sidebar di Windows        | {37efd44d-ef8d-41b1-940d-96973a50e9e0} | Esegue il mapping a Microsoft. DesktopGadgets in Windows 7. Rimosso a partire da Windows 8.                                                                                                                                                                                                                                                                                   |
| Microsoft. WindowsSideShow                                   | Windows SideShow                  | {E95A4861-D57A-4be1-AD0F-35267E261739} | Funzionalità deprecata in Windows 8, rimossa a partire da Windows 8.1.                                                                                                                                                                                                                                                                                               |



 

## <a name="using-canonical-names-in-local-group-policy"></a>Uso di nomi canonici in Criteri di gruppo locali

A partire da Windows 7, è possibile usare i nomi canonici per limitare l'accesso ai singoli elementi del pannello di controllo tramite criteri di gruppo. Questa stessa procedura può essere utilizzata in Windows Vista, ma è necessario utilizzare il nome del modulo anziché il nome canonico.

### <a name="hiding-individual-control-panel-items"></a>Nascondere singoli elementi del pannello di controllo

Utilizzare questo metodo se si desidera visualizzare più elementi del pannello di controllo che si desidera nascondere.

1.  Eseguire il file gpedit. msc per avviare il Editor Criteri di gruppo locali. È anche possibile digitare "criteri di gruppo" nella schermata Start Windows 8.1 e selezionare **modifica criteri di gruppo** nei risultati della ricerca.
2.  Selezionare **Configurazione utente**  >  **modelli amministrativi**  >  **Pannello di controllo**.
3.  Selezionare **Nascondi elementi specificati del pannello di controllo**.
4.  Nella finestra **Nascondi elementi del pannello di controllo specificati** visualizzata fare clic su **abilitato**.
5.  Fare clic sul pulsante **Mostra** nel pannello opzioni per visualizzare l'elenco degli elementi del pannello di controllo non consentiti.
6.  Nella finestra **Mostra contenuto** visualizzata digitare un nome canonico nella colonna **valore** . Ripetere la richiesta.
7.  Fare clic su **OK**.

### <a name="showing-individual-control-panel-items"></a>Visualizzazione di singoli elementi del pannello di controllo

Utilizzare questo metodo se si desidera nascondere più elementi del pannello di controllo che si desidera visualizzare.

1.  Eseguire il file gpedit. msc per avviare il Editor Criteri di gruppo locali. È anche possibile digitare "criteri di gruppo" nella schermata Start Windows 8.1 e selezionare **modifica criteri di gruppo** nei risultati della ricerca.
2.  Selezionare **Configurazione utente**  >  **modelli amministrativi**  >  **Pannello di controllo**.
3.  Selezionare **Mostra solo elementi specificati del pannello di controllo**.
4.  Nella finestra **Mostra solo elementi del pannello di controllo specificati** visualizzata fare clic su **abilitato**. Questa operazione nasconde tutti gli elementi nel pannello di controllo.
5.  Fare clic sul pulsante **Mostra** nel pannello opzioni per visualizzare l'elenco degli elementi del pannello di controllo consentiti.
6.  Nella finestra **Mostra contenuto** visualizzata digitare un nome canonico nella colonna **valore** . Ripetere la richiesta.
7.  Fare clic su **OK**.

Se si desidera rimuovere tutte le voci aggiunte a un elenco Mostra o Nascondi elementi del pannello di controllo, tornare alla schermata nel passaggio 4 e selezionare **non configurato** per cancellare l'elenco. Se si desidera mantenere le voci ma sospendere le restrizioni, selezionare **disabilitato**.

## <a name="remarks"></a>Commenti

È possibile visualizzare gli elementi nel pannello di controllo che non sono elencati qui. Tali elementi non fanno parte di Windows, ma vengono invece aggiunti durante l'installazione di diversi software e hardware, ad esempio Microsoft Office o una scheda video. Gli elementi del pannello di controllo non Windows possono avere o meno un nome canonico. Per trovare il nome canonico di un elemento del pannello di controllo non elencato qui, cercare nel registro di sistema nei percorsi seguenti:

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID of the Control Panel item}
         System.ApplicationName
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         CLSID
            {CLSID of the Control Panel item}
               System.ApplicationName
```

Per ulteriori informazioni che consentono di individuare i CLSID necessari, vedere [come registrare gli elementi del pannello di controllo eseguibile](how-to-register-an-executable-control-panel-item-registration-.md) e [come registrare gli elementi del pannello di controllo dll](how-to-register-dll-control-panel-item-registration-.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esecuzione degli elementi del pannello di controllo](executing-control-panel-items.md)
</dt> <dt>

[**IOpenControlPanel**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel)
</dt> </dl>

 

 



